# redirects-to-blackhole
Send exploit hunting bots to the [Blackhole for Bad Bots](https://en-ca.wordpress.org/plugins/blackhole-bad-bots/) by pre-populating [Redirection](https://en-ca.wordpress.org/plugins/redirection/)'s list of redirects with common exploiter paths.

**eg:** ``REDIRECT 308  /mysqlbackup.zip /?blackhole``

## Requirements
The following Wordpress plugins are required:
1. [Blackhole for Bad Bots](https://en-ca.wordpress.org/plugins/blackhole-bad-bots/)
2. [Redirection](https://en-ca.wordpress.org/plugins/redirection/)

## Installation
1. In Redirection's settings area, on the tab for Import/Export, import the [fu-bots.json](https://github.com/JayHoltslander/redirects-to-blackhole/blob/master/fu-bots.json) list. This can be found at ``https://[YOURDOMAIN.COM]/wp-admin/tools.php?page=redirection.php&sub=io``
2. After importing the list you will have a new group of redirects called BLACKHOLE REDIRECTS. You can manage the group at ``https://[YOURDOMAIN.COM]/wp-admin/tools.php?page=redirection.php&sub=groups`` If you ever update your list from this repo in the future you should delete the entire group first. This is because the import operation does not have merge capabilities.

Now any bots that try to visit any of those common exploiter paths will be redirected to the blackhole trap and then immediately perma-banned on arrival.

## What you can expect after
Bots will soon be caught probing around and hitting these common exploit paths and being blocked for trying.

![Screenshot](screenshot.png)
