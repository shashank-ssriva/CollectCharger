# CollectCharger
A Mac reminder app written in Python3 to remind you to collect your charger before you leave your workplace.

# Introduction
How often do you forget your charger (or any other item) at your workplace only to regret later? I have a pretty bad habit of forgetting my mobile charger at my desk which I only come to know about when I am in the cab on my way back home. I even once forgot to take my charger with me before leaving for a week long trip to Manali :smile:  
So today, I wrote a tiny Python script which runs in the background and sends me a reminder at a particular time by popping up a system notification along-with a beep & speaking it out loud :satisfied:  
This script is written for Mac only but can be easily customised for any other Linux based OS.

# Requirements
This script depends on ``terminal-notifier`` to display system notification. To install it, issue...
```bash
admin@shashank-mbp ~> brew install terminal-notifier
```

# Usage
To run it, just copy the Python script to a directory & tuck it inside a Cron job. I leave my workplace at 14:30, so I set the Cron job as : - 
```bash
15 14 * * 1-5 /usr/local/bin/python3 /Users/admin/Desktop/PythonScripts/ChargerCollect.py >/Users/admin/Desktop/reminder_cronout.log 2>/Users/admin/Desktop/reminder_error.log
```

This notifies me to collect my charger at 14:15 :-)

# Acknowledgement
I took some help from below Stack Overflow answer by [Peter Varo](https://stackoverflow.com/users/2188562/peter-varo).
https://stackoverflow.com/questions/17651017/python-post-osx-notification

Thanks Peter (*if you are reading this*) for your answer! If there is any other way to say thanks or give credit to your answer, please let me know!
