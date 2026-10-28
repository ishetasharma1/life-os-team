# Setting up "health-daily" (about 10 minutes, once)

Your smart scale, Apple Watch and Garmin/Fitbit/Oura all sync into Apple Health. An iPhone Shortcut copies yesterday's numbers into a Google Sheet each morning, and the Health & Fitness Coach reads that sheet.

1. **Sync devices into Apple Health.** Scale app (Withings/Renpho/etc.), Garmin Connect, Fitbit (via a sync app) or Oura: in each app turn on "Apple Health" writing for weight, body fat, steps, sleep, resting heart rate and workouts.
2. **Create the sheet.** Google Sheet named `health-daily`, columns: Date · Weight kg · Body fat % · Steps · Sleep h · Resting HR · Workout min.
3. **Build the Shortcut** (Shortcuts app → Automation → Time of Day 06:30, run immediately): "Find Health Samples" for each metric (yesterday; weight = latest today), then "Get contents of URL" posting one row to the sheet through a Google Apps Script web app, or use the "Google Sheets → Add row" action if you have an integration app.
4. **Test** once; the coach confirms it can read the row in the next Evening Huddle.

If a day is missing, the coach writes "not logged" and asks you.
