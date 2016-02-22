---
layout: post
---

Last version we've talk about was [v3](http://blog.cloudcmd.io/post/cloud-commander-v3 "v3").
Todays most acutal version is [v5.1.2](https://github.com/coderaiser/cloudcmd/releases/tag/v5.1.2 "v5.1.2") and
what is happen with `Cloud Commander` during 2 major releases and a lot minors and patches it is main topic of todays talk.

## Logout

That is right. Context menu has logout item that will clear `http-auth` headers when you will click it starting from [v3.2.0](https://github.com/coderaiser/cloudcmd/releases/tag/v3.2.0 "v3.2.0")

## Middleware

`Cloud Commander` could be used as `express` middleware, feel free to experiment :).

```js
var http        = require('http'),
    cloudcmd    = require('cloudcmd'),
    express     = require('express'),
    io          = require('socket.io'),
    app         = express(),

    PORT        = 1337,
    PREFIX      = '/cloudcmd',
    server,
    socket;

server = http.createServer(app);
socket = io.listen(server, {
    path: PREFIX + '/socket.io'
});

app.use(cloudcmd({
    socket: socket,
    config: {
        prefix: PREFIX,
    }
}));

server.listen(PORT);
```

## Files packing

You can pack couples files starting from [v3.7.0](https://github.com/coderaiser/cloudcmd/releases/tag/v3.7.0 "v3.7.0"). Nice feature to have.


# Directories

You can download folders as archives starting from [v3.8.0](https://github.com/coderaiser/cloudcmd/releases/tag/v3.8.0 "v3.8.0").
And upload directories via drag'n'drop from [v4.1.0](https://github.com/coderaiser/cloudcmd/releases/tag/v3.8.0 "v4.1.0").

# HTML Dialogs

[v4.6.0](https://github.com/coderaiser/cloudcmd/releases/tag/v4.6.0 "v4.6.0") bring ability to use `html dialogs` with help of [smalltalk](http://github.com/coderaiser/smalltalk "smalltalk")

![Smalltalk](https://raw.githubusercontent.com/coderaiser/smalltalk/master/screen/alert.png "Smalltalk")

# Date of modification

In [v5.1.0](https://github.com/coderaiser/cloudcmd/releases/tag/v5.1.0 "v5.1.0") date columnt appered with help of [readify](https://github.com/coderaiser/readify "readify") and [shortdate](https://github.com/coderaiser/shortdate "short date") help.

![Date](http://files.cloudcmd.io/img/2016-02-21-cloud-commander-v5.1.2/date-column.png "Date Column")

# That's all folks

That is all for today folks. Subscribe to [twitter](https://twitter.com/cloudcmd "twitter") follow on [github](https://github.com/coderaiser/cloudcmd "github") and have a lot fun :).

