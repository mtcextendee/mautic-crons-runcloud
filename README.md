# Mautic crons on RunCloud

This script install crons runs every minute for command:

- mautic:segments:update
- mautic:campaigns:update
- mautic:campaigns:trigger

Don't forget edit first line of directory name of your app.

```
DIR="mautic";
wget -N https://raw.githubusercontent.com/mtcextendee/mautic-crons-runcloud/master/crons.txt;
(crontab -l; echo "$(< crons.txt)"|replace DIR "$DIR")| crontab -;
unlink crons.txt;crontab -l;
```
