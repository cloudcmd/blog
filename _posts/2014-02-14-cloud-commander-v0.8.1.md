---
layout: post
---

Fist of all I want admit new font icons you could see on menu and commands buttons.
This should do UI of file manager more userfriendly. Hope it does :).

![Edit](http://screen.cloudcmd.io/cloudcmd-v0.8.0-menu.png "Menu")

Next thing is [combine](http://blog.cloudcmd.io/post/cloud-commander-v0.7.0/)
is now called **join** it shorter and simpler. But still very usefull.

In this release speed was enhanced with `exec` function of `Util` module.
This is how it looks now:

```js
this.exec                       = function(callback) {
    var ret,
        args    = Util.slice(arguments, 1);
   
    if (Util.isFunction(callback))
        ret     = callback.apply(null, args);
    
    return ret;
};
```

Simple, easy to use and do just one thing.
Becouse of many things depends on this function it's pretty good optimizitaion.

With help of function `changeUIDToName` *nix users could see names, not just uids.
Thing this function do is pretty simple: parse `/etc/passwd` file
and gets names from it (do it only if date of last parsed file is changed).

All tests was fixed. But it's not a big thing ofcorse.

What is more interesting, is ability to select files `*`, `+` keys and
deselect them whith `-` key. All this things works with simple file formats, you
actualy know it: `*.*` - for any file whith any extension etc.

`CloudCmd.View` sometimes after show looks very strange and start tweaking.
This was fixed by changing config paramter `loop:false` and adding this function:

```js
function rmKeys() {
    $.fancybox.defaults.keys = null;
}
```

Which do next thing: if some symbol keys was pressed loop begins.

As always code of file manager is more stable now, more easy to mantain and more
userfriendly. Happy using :).

By the way, almost forgat, you could watch [screenshots history](http://screen.cloudcmd.io "Screenshots history") of file manage in newly created page.

You could download last verion of Cloud Commander from this [link](https://github.com/coderaiser/cloudcmd/releases/tag/v0.8.1 "Cloud File manager").
