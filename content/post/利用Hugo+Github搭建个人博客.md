+++
date = '2026-01-09T00:54:57+08:00'
draft = true
title = '利用Hugo+Github搭建个人博客'
+++

# 利用Hugo+Github搭建个人博客站









```bash
root@eve-ng:~/My-Blog# ssh -T git@github.com
Hi liupc356! You've successfully authenticated, but GitHub does not provide shell access.
```





```bash
root@eve-ng:~/my-blog/quickstart# hugo server --bind 192.168.1.199 --port 1313 --buildDrafts 
Start building sites … 
hugo v0.92.2+extended linux/amd64 BuildDate=2023-01-31T11:11:57Z VendorInfo=ubuntu:0.92.2-1ubuntu0.1
WARN 2026/01/07 21:37:21 found no layout file for "HTML" for kind "home": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
WARN 2026/01/07 21:37:21 found no layout file for "HTML" for kind "page": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
WARN 2026/01/07 21:37:21 found no layout file for "HTML" for kind "taxonomy": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
WARN 2026/01/07 21:37:21 found no layout file for "HTML" for kind "section": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
WARN 2026/01/07 21:37:21 found no layout file for "HTML" for kind "taxonomy": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.

                   | EN  
-------------------+-----
  Pages            |  4  
  Paginator pages  |  0  
  Non-page files   |  0  
  Static files     |  0  
  Processed images |  0  
  Aliases          |  0  
  Sitemaps         |  1  
  Cleaned          |  0  

Built in 3 ms
Watching for changes in /root/my-blog/quickstart/{archetypes,content,data,layouts,static}
Watching for config changes in /root/my-blog/quickstart/config.toml
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 192.168.1.199)
Press Ctrl+C to stop
WARN 2026/01/07 21:37:24 found no layout file for "HTML" for kind "home": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.

^C
```







```bash
root@eve-ng:~/my-blog/quickstart# hugo server --bind 192.168.1.199 --port 1313 --verbose
Error: add site dependencies: load resources: loading templates: "/root/my-blog/quickstart/themes/ananke/layouts/_partials/func/style/GetMainCSS.html:54:1": parse failed: template: _partials/func/style/GetMainCSS.html:54: function "css" not defined
```





```bash
erbose
ERROR deprecated: --verbose was deprecated in Hugo v0.114.0 and will be removed in Hugo 0.139.0. use --logLevel info
WARN  Module "ananke" is not compatible with this Hugo version: Min 0.146.0; run "hugo mod graph" for more information.
Watching for changes in /root/my-blog/quickstart/{archetypes,content,data,layouts,static,themes}
Watching for config changes in /root/my-blog/quickstart/hugo.toml, /root/my-blog/quickstart/themes/ananke/config/_default
Start building sites … 
hugo v0.138.0-ad82998d54b3f9f8c2741b67356813b55b3134b9+extended linux/amd64 BuildDate=2024-11-06T11:22:34Z VendorInfo=gohugoio

INFO  static: syncing static files to / duration 819.636µs
INFO  build:  step process substep collect files 1 files_total 1 pages_total 1 resources_total 0 duration 1.037308ms
INFO  build:  step process duration 1.100109ms
INFO  build:  step assemble duration 414.814µs
WARN  found no layout file for "html" for kind "taxonomy": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
WARN  found no layout file for "html" for kind "section": You should create a template file which matches Hugo Layouts Lookup Rules for this combination.
ERROR render of "home" failed: "/root/my-blog/quickstart/themes/ananke/layouts/baseof.html:26:15": execute of template failed: template: home.html:26:15: executing "home.html" at <partials.Include>: error calling Include: partial "site-style.html" not found
INFO  build:  step render pages 3 content 0 duration 7.630736ms
INFO  build:  step render deferred count 0 duration 956ns
INFO  build:  step postProcess duration 10.067µs
INFO  build:  duration 9.343028ms
Built in 9 ms
Error: error building site: render: failed to render pages: render of "404" failed: "/root/my-blog/quickstart/themes/ananke/layouts/baseof.html:26:15": execute of template failed: template: 404.html:26:15: executing "404.html" at <partials.Include>: error calling Include: partial "site-style.html" not found
```


