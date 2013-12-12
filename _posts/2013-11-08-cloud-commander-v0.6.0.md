---
layout: post
---

![Config](http://cloudcmd.io/img/screen/config.png)
Since [last version](http://blog.cloudcmd.io/post/cloud-commander-v0.5.0 "Cloud Commander v0.5.0") of [Cloud Commander](http://cloudcmd.io "Cloud Commander") was released a month ago so today is time for new version. It could be downloaded [here](https://github.com/coderaiser/cloudcmd/releases/tag/v0.6.0 "Cloud Commander v0.6.0"). Lets talk about fixes and features.
Fix
------
- When somebody go to url **api/v1** Commander has been crashed.
- Header was send twice all the time it's wrong.

Features
------
- From now configuration is a little bit more pleasure process, because
you could run it's window with **F10** key press or if you click on the
button. Of Course you could edit file **json/config.json** if you want.
- Express was added to Commander. And thing makes hime little bit faster.
You could not install it, Commander will work without express to,
but a little bit slower.
- Changed the way css file is minifed. From now the would not do it
on every start. Just when it's real needed.
- Changed the way process are started from command line.
[Exec](http://nodejs.org/api/child_process.html#child_process_child_process_exec_command_options_callback "Exec")
function of node it's good choice. But there is no streaming with exec. So if you run command which
would produce a lot of data in stdout. So:
  - it would be slow and you will see result only at the end.
  - buffer could be ended.

So now [Spawn](http://nodejs.org/api/child_process.html#child_process_child_process_spawn_command_args_options "Spawn") function has been added so if symbols like: *"#, {, }, &, >, <"* would be used - spawn would be called. Everything would be much faster with streams.

That's all for today. Would be seen soon :).
