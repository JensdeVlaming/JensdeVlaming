# Notes
In this file I keep all my notes: <br>
<a href="https://github.com/JensdeVlaming/JensdeVlaming/blob/main/notes.md#crontab">Crontab</a>

## Crontab

To add new automation:
```bash
> crontab -e 
```
! Vim wil open: press i to edit file. Press esc to go out of edit mode. Press :x to save and exit and press :q! to exit without saving.
```bash
* * * * * /usr/local/bin/python3 /setup.py
| | | | | 
| | | | |
| | | | |
| | | | day of the week (0 - 6) (Sunday to Saturday; 7 is also Sunday on some systems)
| | | month (1 - 12)
| | day of the month (1 - 31)
| hour (0 - 23)
minute (0 - 59)
```

## Automating with module: schedule and time
```bash
import schedule
import time

def automation():
    print("Automated message")

schedule.every(1).minutes.do(automation)
#schedule.every().hour.do(automation)
#schedule.every().day.at("10:30").do(automation)
#schedule.every(5).to(10).minutes.do(automation)
#schedule.every().monday.do(automation)
#schedule.every().wednesday.at("13:15").do(automation)
#schedule.every().minute.at(":17").do(automation)

while True:
    schedule.run_pending()
    time.sleep(1)
```
