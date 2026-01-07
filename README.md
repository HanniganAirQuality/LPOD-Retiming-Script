# LPOD Retiming Script
This code specifically deals with the problems encountered by the incoming formatting associated with the Particle webhooks integration, Google Sheets & Excel .csv translations. 

## Before Running Script!!
**Please consolidate all of your .csv files into one mega-file.** I do this by using (shudder) Powershell. You can go to the repository, right click & press 'Open Terminal' but it will actually open Windows Powershell (evil) & I have no idea why!!! This has different syntax than Command Prompt. In Command Prompt we'd write: "copy *.csv PODID.csv" but in Powershell we have to write "Get-Content *.csv | Set-Content PODID.csv" -- note that some people warn against using the same suffix so that you don't enter an infinite loop, and I personally have not run into that so whatevs.

## Changing Variables for First Run 
### Required:
1. Line 16: 'PODID.csv' --> name of your mega-file
2. Line 39: Correct final variable names - **do not** change DateTime!!
3. Line 50: Update SENT variable to the correct # of rows that have the same timestamp (my example is 19, but please count to double check)
4. Line 51: Update t_interval to the interval that you know your monitor uses - I recommend referencing a SD file for this, but if not, it's safe to start with the interval from the monitor's interval & add about half a second
5. Line 71: 'POD_YYYY-MM-DD.csv' --> name of completed file, preferably diff from mega-file

### Optional: 
1. Line 46: togglable save in case you have a huge file or you are troubleshooting
2. Line 75: togglable timetable translation that I use for initial plotting to make sure all looks normal-ish
