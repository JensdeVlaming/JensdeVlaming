# Notes
In this file I keep all my notes:
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
