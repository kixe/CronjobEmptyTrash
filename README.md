CRONJOB EMPTY TRASH
===================

Auto delete trashed pages sustainably after a predifined period of time set in module settings.
This cronjob will run once per day.

This cronjob (based on Lazy Cron) will only be executed by a call to module: 'Process Page View'.
By default this module runs only if current user has page-delete permission.

## Settings
**Deletion Deadline** Select the period of time pages will remain untouched in the trash.
**Global trigger** Check this to trigger this cronjob by every user (guest)

## Require
**LazyCron.module**

## License
[GNU-GPLv3](http://www.gnu.org/licenses/gpl-3.0.html)

## Author
kixe (Christoph Thelen)
