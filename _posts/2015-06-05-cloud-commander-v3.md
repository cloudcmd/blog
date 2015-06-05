---
layout: post
---

I wrote nothing for so long and today I'm going to fix things up.
In new version you will find progress of copying (at last :)!).
And a lot big and small improvements. Actually some feature was released
some time ago (a couple releases back). But I haven't wrote about it, and I think
now is the best time for it.

## Config
First of all take look at new config window.

![Config](http://files.cloudcmd.io/img/2015-06-05-cloud-commander-v3/config.png "Config")

## Progress of copying

As you see, you could enable **Progress of copying** checkbox to use new way of copying.
When this option enabled you can see progress when copy files.
[Spero](https://github.com/cloudcmd/spero "Spero") makes possible such things.
It joins module for copying with ability to handle progress [copymitter](https://github.com/coderaiser/copymitter "Copymitter") and
[socket.io](http://socket.io "Socket.io") to interchange data with frontend part of
Cloud Commander.

## Editors

You can choose editor you want: [Edward](https://github.com/cloudcmd/edward "Edward")(based on [Ace](http://ace.c9.io "Ace")) or [Dword](https://github.com/cloudcmd/dword "Dword")(based on
[CodeMirror](http://codemirror.net "CodeMirror")).

This two modules makes different API of editors work in the same way. Now they can compete
with each other on fair. And you have to chose from.

## File System Root

You could set (and dinamically change) root of File System Cloud Commander work with.
This feature supports Unix and Windows as well.
So if you prefer directory different from root (your home directory for example).
You could set it.

## Command line

After you had bean installed cloudcmd with:

```
npm i cloudcmd -g
```

Try:

```
man cloudcmd
```

That's right. Cloud Commander supports [man pages](http://en.wikipedia.org/wiki/Man_page "Man Pages").
One more new thing it's options, you could set them from command line:

```
coderaiser@cloudcmd:~/cloudcmd$ cloudcmd -h
Usage: cloudcmd [options]
Options:
  -h, --help      display this help and exit
  -v, --version   display version and exit
  -s, --save      save configuration
  -o, --online    load scripts from remote servers
  -a, --auth      enable authorization
  -u, --username  set username
  -p, --password  set password
  -c, --config    configuration file path
  --editor        set editor: "dword" or "edward"
  --root          set root directory
  --port          set port number
  --no-auth       disable authorization
  --no-server     do not start server
  --no-online     load scripts from local server
  --minify        enable minification
  --no-minify     disable minification
  --progress-of-copying show progress of copying
  --no-progress-of-copying not show progress of copying

General help using Cloud Commander: <http://cloudcmd.io>
```

You could define all options, set flag `--save` and just use Cloud Commander
with predefined options. All of them will be saved in `~/.cloudcmd.json` file.

**Tip**
Do not set password by manually editing config file it will not work if you
will not crypt it first.

## Releases

There is two little helpers that all do hard work related with releases:
[wisdom](https://github.com/coderaiser/wisdom) and [runny](https://github.com/coderaiser/node/node-runny). First handle all
casual staf of making tags, realeses, push to github and publish to npm.
And second one runs one command in a couple directories. So I could update
[cloudcmd.io](http://cloudcmd.io "cloudcmd.io") with Russian and Ukrainian
translation, publish new version to npm, and add new version to [versions archive](https://github.com/cloudcmd/archive "Versions Archive") with one simple command:

```
runny --command "wisdom patch" --directories "~/cloudocmd,/~cloudcmd-io,~/ru,~/ru-io,~/ua,~/ua-io,~/archive"
```

Actually directories could be placed to `~/.runny.json`:
```js
{
    "directories": [
        "~/cloudcmd",
        "~/ru",
        "~/ua",
        "~/ru-io",
        "~/ua-io",
        "~/cloudcmd-io",
        "~/archive"
    ]
}
```

And command would be as simple as:

```
runny --command "wisdom patch"
```

## Afterword

This is all for today.
You can always send me [pull requests](https://github.com/coderaiser/cloudcmd/pulls "Pull request"), [make issues](https://github.com/coderaiser/cloudcmd/issues "Issues"), ask questions, send mail etc.
