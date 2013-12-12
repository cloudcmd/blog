---
layout: post
category : post
---

A couple days ago new version of [Cloud Commander](http://cloudcmd.io "Cloud Commander") was released. So you can download last stable version on [this](https://github.com/coderaiser/cloudcmd/releases/tag/v0.4.0 "v0.4.0") page. New [demo](http://io.cloudcmd.io "demo") page was added so feel free to test and look around.

Lets talk a little bit about improvements.
In [config](https://github.com/coderaiser/cloudcmd/blob/master/json/config.json#L4L5 "config") was added two new fields:

 -  localStorage
 - analytics

Which are sett to true by default (as like that was earlier). 
But you can turn off any of this options any time.

Maximum re-connection attempts of web sockets was increased so if connection would be lost, it come back when server would be started again.

Buttons **F5** (Copy) and **F6** (Move) are hiding when Cloud Commander works in one-panel mode.

Auto updating system was changed from
``` git pull ``` to ```git pull --rebase``` so any commits would not be removed any more (but you will need to stash any change).

From now you could upload files via drag'n'drop. Just take file on desktop, move it in Cloud Commander and drop it. By the way downlod file to desktop doing in same way but in back order.

Funny and very useful routes was added:

- [menu](http://io.cloudcmd.io#/menu "Menu")
- [console](http://io.cloudcmd.io#/console "Console")
- [edit](http://io.cloudcmd.io/fs/etc#/edit/passwd "Edit")

Removed **jquery-migrate** dependency so it would not load any more.

And last improvement for today. "Nothing to save" was removed from editor because it has no sense.