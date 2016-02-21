---
layout: post
---

Cloud Commander [v1.2.0](https://github.com/coderaiser/cloudcmd/releases/tag/v1.2.0) is out.
During time between releases a lot work was done about decomposition of server side.

On the way a lot modules where made and published on npm. We will talk about it today.
Another big changes was with config, and a little bit new features would be too.

## Buffer

Let's start from buffer. If you use one panel (on mobile device, for example) from now,
you could copy and move files and folders. You could do it in two panels too by
using menu or hot keys `Ctrl + x`, `Ctrl + c`, `Ctrl + v`, `Ctrl + z`.


## New Config

Becouse of new **Buffer** functions and fact, that it depends on `localStorage`, new options in **Config**
were added.

![Config](http://files.cloudcmd.io/img/2014-08-29-cloud-commander-v1.2.0/config.png "Config")

As you can see `appCache` was removed, and `Directory Storage` and `Buffer` was added.
`Directory Storage` was enabled by default, but now it could be disabled. This option
adds ability to store directory listeings to `localStorage`. But not everybody things
it's useful, so now can rule it whenever you like :).

## New Menu

![Menu](http://files.cloudcmd.io/img/2014-08-29-cloud-commander-v1.2.0/menu.png "Menu")

Not only **Config** changed. To **Menu** a couple items was added:

- cut
- copy
- paste

For work with **Buffer**.

## New node modules

Last time we [talked about node modules](http://blog.cloudcmd.io/post/cloud-commander-v1.0.0/ "Node modules").

- [ischanged](https://github.com/coderaiser/ischanged "Ischanged") - Is file changed check;
- [ponse](https://github.com/coderaiser/ponse "Ponse") - module for work with requests and responses;
- [files-io](https://github.com/coderaiser/files-io "Files") - read many files in node;
- [nicki](https://github.com/coderaiser/nicki "Nicki") - get names of users by uids from /etc/passwd;
- [pipe-io](https://github.com/coderaiser/pipe-io "Pipe-IO") - pipe streams and handle events;
- [timem](https://github.com/coderaiser/timem "Time M") - get file modification time;
- [join-io](https://github.com/coderaiser/join-io "Join-IO") - join files on a fly to reduce requests count;
- [console-io](https://github.com/cloudcmd/console "Console-IO") - web console;
 
About most interesting modules we should talk a little bit more.

## Join

After `combine` was renamed to `join` as mentioned in [v0.8.1](http://blog.cloudcmd.io/post/cloud-commander-v0.8.1/ "Combine renamed to Join"),
it was released as middleware for `express`.

If you want join a couple styles to 1 request, `join url` will look like this:

`<link rel="/join:/css/normilize.css:/css/style.css">`

To improve download spead minification could be used, `join-io` uses [minify](http://coderaiser.github.io/minify "Minify")
which minify only when it's realy needed.

## Console-io

Now you could use `console` from **Cloud Commander** as express middleware. You could embed it to any page you want.
It's as simple as this code on server:

```js
app.use(webconsole(server));
```

And this on client:

```html
<div class="console"></div>
<script src="/console/console.js"></script>
<script>
    Console('.console', function() {
        console.log('console ready')
    });
</script>
```

## Afterword

I hope you appreciate all this things. It's not so easy, but realy funny. Have a good time using
all this stuff. That is all for today :).
