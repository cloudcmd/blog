---
layout: post
---

Today is a big day. Cloud Commander version is [1.0.0](https://github.com/coderaiser/cloudcmd/releases/tag/v1.0.0).
It's realy stable, I'm not kidding you :). I use it for work on my projects, write articles like [this one in Russian](http://habrahabr.ru/post/226257/).

I hope you will be happy with improvements and fixes it has. If not feel free to make [issue](https://github.com/coderaiser/cloudcmd/issues/new),
pull requests are wellcome. Lets talk about new things that are waiting for you in this big release.

## New look of Refresh and Clear Storage icons

![Edit](http://files.cloudcmd.io/img/2014-07-03-cloud-commander-v1.0.0/path-buttons.png "Path Buttons")

That's right. This icons hasn't changed so long time. Thay was with us almost from the start.
But the time is come for changing and now this icons is part of one Font icons set.

## Pathes in Console

![Console](http://screen.cloudcmd.io/cloudcmd-v1.0.0-console.png "Console")

One more big change is console. Which is shows pathes in Windows, Linux and Mac.
You could relax and stop typing `pwd` all the time to know in what directory
are you now, like it was with me.

## Volumes on Windows

If you worked in Windows you could notice that in Cloud Commander was not
support of volumes. That is right. Only one volume, where process started.
And that is all. But it's not fair for windows users.

For now volumes support would be integral part of Cloud Commander,
I'll do my best for it.

![Console](http://screen.cloudcmd.io/cloudcmd-v1.0.0.png "Cloud Commander v1.0.0")


## Node modules

I mention that there is no way to get windows volumes in node.js. So I published
new module called [win32](http://github.com/coderaiser/win32).
All it's do is try to get windows volumes this way:

```js
var win = require('win32');

win.getVolumes(function(error, volumes) {
    console.log(error, volumes);
});

```
It's must work properly from Windows XP to Windows 8. That's all I have tested.

It is not last module for today. There are full list of newly published modules
which was part of Cloud Commander for a long time:

- [flop](http://github.com/coderaiser/flop "Flop") - folder operations module
- [format-io](http://github.com/coderaiser/format-io "Format") - format size, permissions, etc
- [trammel](http://github.com/coderaiser/trammel "Trammel") - get directory size

## Junshi - mac os client

![Junshi](https://raw.githubusercontent.com/coderaiser/junshi/master/img/junshi.png "Junshi")

I want try something new and start working on [Mac OS client](https://github.com/coderaiser/junshi "Mac OS Client") for Cloud Commander.
It's very simple for now. I'm new to `Objective C` so pull requests are welcome :).

## Shinju - node client

Work with Cloud Commander from terminal? No problem! You could try [client for Cloud Commander's console](https://github.com/coderaiser/shinju).
All you need is running server part. It would looks like in build-in terminal:

```sh
> shinju http://localhost:8000

/home/coderaiser/cloudcmd> ps
  PID TTY          TIME CMD
  661 pts/0    00:00:00 ps
32199 pts/0    00:00:00 bash
32622 pts/0    00:00:01 node

/home/coderaiser/cloudcmd> whoami
coderaiser

/home/coderaiser/cloudcmd>
```

## End words

I created [wiki](https://github.com/coderaiser/cloudcmd/wiki "Wiki") at Cloud Commander's repository.
Feel free to add some information and thoughts.

That is all for today. Happy using :).
