# Setting up "health-daily" (about 20 minutes, once)

Sheet (created 28 Oct 2026): https://docs.google.com/spreadsheets/d/1WfS22vSWK5Xgq1sdEXabsE63vlLQeES5r2Iox1VihD8/edit
Columns: Date · Weight kg · Body fat % · Steps · Sleep h · Resting HR · Workout min. The iPhone Shortcut adds one row a day at 20:00, before the 20:23 Evening Huddle.

## 1. Devices → Apple Health
- Smart scale app (Withings, Renpho, Eufy…): Settings → Apple Health → allow weight and body fat.
- Garmin Connect: More → Settings → Connected Apps → Apple Health → turn on.
- Oura: Settings → Apple Health → turn on.
- Fitbit: does not write to Apple Health directly; needs a sync app (e.g. "Health Sync for Fitbit") or skip it.
- Apple Watch: automatic.

## 2. Apps Script (receives the data)
In the sheet: Extensions → Apps Script → replace everything with the code below → choose your own secret word instead of CHANGE-ME → Save.

```javascript
function doPost(e) {
  var d = JSON.parse(e.postData.contents);
  if (d.key !== 'CHANGE-ME') return ContentService.createTextOutput('denied');
  var sh = SpreadsheetApp.getActiveSpreadsheet().getSheets()[0];
  sh.appendRow([d.date, d.weight, d.bodyfat, d.steps, d.sleep, d.rhr, d.workout]);
  return ContentService.createTextOutput('ok');
}
```

Deploy → New deployment → gear icon → Web app → Execute as: Me · Who has access: Anyone → Deploy → Authorise (Advanced → Go to project → Allow) → copy the Web app URL. The secret word stops anyone else with the link from writing to your sheet.

## 3. The Shortcut (Shortcuts app → Automation → + → Time of Day 20:00, Daily → Run Immediately → New Blank Automation)
1. Find Health Samples: Type Weight · Start Date is today · Sort Latest First · Limit 1.
2. Find Health Samples: Type Body Fat Percentage · today · Latest First · Limit 1.
3. Find Health Samples: Type Steps · today → Calculate Statistics: Sum.
4. Find Health Samples: Type Sleep Analysis · Start Date in the last 1 day · Value is not In Bed · Value is not Awake → Calculate Statistics: Sum (duration).
5. Find Health Samples: Type Resting Heart Rate · today · Latest First · Limit 1.
6. Find Health Samples: Type Exercise Minutes · today → Calculate Statistics: Sum.
7. Format Date: Current Date · Custom · yyyy-MM-dd.
8. Get Contents of URL: your Web app URL · Method POST · Request Body JSON with Text fields: key (your secret word), date (Formatted Date), weight (step 1 → Value), bodyfat (step 2 → Value), steps (step 3 result), sleep (step 4 result, in hours), rhr (step 5 → Value), workout (step 6 result).
Turn off "Notify When Run".

## 4. Test
Run the automation once by hand; a row should appear in the sheet. If Shortcuts shows an error but the row is there, that's Google's redirect and harmless. If a value is blank (e.g. no weigh-in that day), the coach treats it as "not logged".
