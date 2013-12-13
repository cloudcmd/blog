---
layout: post
---

Let's talk about new [version](https://github.com/coderaiser/cloudcmd/releases/tag/v0.7.0 "0.7.0"). A couple things was fixed but features is great for real in this version. Today we will talk about such features
as **Combine**, **localStorage** and **Notification**. First one is feature of Commander, and others is HTML5.

Combine
------------
if you go to url **/combine** you could combine a couple files in one. So 
it would load much faster then bunch files on separate requests.
So for styles it looks like this:

```
/combine + /css/reset.css + :  + css/style.css
```

Complete url would be:
```
http://io.cloudcmd.io/combine/css/reset.css:css/style.css
```

Same thing for JavaScript.
All this things could be possible because of node [streams](http://nodejs.org/api/stream.html "Stream").


Local Storage
------------
Next big thing is the way Local Storage is used in Cloud Commander.
Folders content is saving to Storage on first came. It's not a big deal. 

But for now files content is saves to Storage to :). If option localStorage in **config** is set to "true".

When file is opened for first time it's content is saved to localStorage with hash tag. When you try to save something (add **diff** options is enabled), diff of file content is send to server, and new hash is getting up. So work with files should be much faster then is was.


Notifications
------------
That's right, same notifications as [GMail](http://gmail.com "GMail") use for delivering message to Google Talk users.
So, if you enable in Config this option, and would wright something in console with symbol **#** at begin, this message would be send to all connected users. And if some of them would be on other ten Commander tab, Notification would appear.

That is all for today. Have fun :).
