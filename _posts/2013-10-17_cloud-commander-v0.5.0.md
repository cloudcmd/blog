---
layout: post
---

So the day of new release of [Cloud Commander](http://cloudcmd.io "Cloud Commander") is came.  You could download it from [here](https://github.com/coderaiser/cloudcmd/releases/tag/v0.5.0 "here").
Let's talk a little bit about new features.

1. Render was changed from "{, }" to [handlebars](http://handlebarsjs.com/ "handlebars") style, which is "{{, }}".
Thing is [jekyll](http://jekyllrb.com "Jekyll") use it by default. So because [cloudcmd.io](http://cloudcmd.io "Cloud Commander") works on Jekyll as like [Ukrainian](http://ua.cloudcmd.io "Ukrainian") and [Russian](http://ru.cloudcmd.io "Russian") translations. It's better to use single style.

2. Add **noindex** and **nofollow** meta tags to index html. So no search bots would came to **Commander** and this is good.

3. Add menu item  **(Un)Select All** for Selection and UnSelection of files.

4. Changed jqueryLoad so if there is no network connection [jQuery](http://jquery.com "jQuery") will load from local server not remote.

5. retExec and retFunc now can get any count of parameters.

6. Add **online** option to config. So if it set to false. **jQuery** would load from local server.

7. Changed **minification** option on **Config** to **minify** and now it's boolean. There is no sense for manual setting up minifycation of such resources as **css**, **html** etc.

8. [Minify](http://coderaiser.github.io/minify "Minify") updated to v0.2.2

That is all for today. Be careful, if you would update Commander, please change Config file because this version is not compatible with old ones.
