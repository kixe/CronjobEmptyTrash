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

## Bugs

### 1: function is called twice. double entry in log file (message.txt)
### 2: message cannot be displayed because lazycron hooks in pageView::finished and not in PageView::ready

## Development notices

### 1: difference?
´´´
		//$trashed = $this->wire('pages')->find('parent=7, include=all');
		$trashed = $this->wire('pages')->find('status>=8192, include=all');
´´´

### 2: 
´´´
		//$display=($this->wire('user')->isSuperuser)?true:false;
		//$display = true;
		$this->message($message,true);
		
		//statusTrash = 8192
		//statusDeleted = 16384
		//trash page id = 7


´´´

		

