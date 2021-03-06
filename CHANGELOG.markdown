Table of Contents
=================

* [v0.7.2](#v0.7.2)
* [v0.7.1](#v0.7.1)
* [v0.7](#v0.7)
* [v0.6](#v0.6)
* [v0.5](#v0.5)
* [v0.4](#v0.4)
* [v0.3](#v0.3)

v0.7.2
======

> Date: 2019.03.08

* doc: added the annotations about the compatibilty for the blocking phases.
* change: updated the lua-resty-socket dependency.
* bugfix: fixed the bootless keep-alive feature, now it works when the
condition is conformed.

v0.7.1
======

The old version is not so semantic, now we tweaked it.

> Date: 2019.02.21

This version just contains some minor improvements.

* doc: fix timeout misrepresent, seconds => milliseconds. Thanks jetz for the
patch.
* doc: README fix typo ("Authorization") 7 hours. Thanks Chris Kuehl for the
patch.
* doc: fixed some documentary typos.
* feature: used lua-resty-socket when the phase is not yieldable.
* feature: used cosocket pool backlog if the ngx_lua is new enough.

v0.7
====

> Date: 2018.12.03

This version refactored the logic about headers indexing, also fixed the relevant bug.

* refactored the request/response headers table logic.

v0.6
====

> Date: 2018.11.15

This version added some new features like r:json(), HTTPS proxy and some bugfixs.

* feature: supported HTTPS proxy based on HTTP CONNECT method.
* feature: r:json(), now one can get a Lua table which deserializes the response body from calling this method.
* feature: added a new option "use_default_type" to control whether adds a default content-type request header when request body exists.
* bugfix: the ttfb metric always records the "time to first header".
* bugfix: add "charset; utf-8" check to json response object "content-type" header, thanks Happy Totem for the report and pull request.

v0.5
====

> Date: 2018.10.25

This version has minor modifications but with a compatibilty broken change.

* change: Content-Length header will not be deleted even when users are using the function request body fashion.
* improve: now we don't launch ssl handshake if a reused connection is using.
* bugfix: http2.lua cannot be copied to the correct openresty lualib dir.

v0.4
====

> Date: 2018.10.09

This version supplemented more test cases and introduced the following
features.

* feature: supported the test of Expect request header.
* feature: supported installation from LuaRocks.
* feature: intergrated with lua-resty-http2, can use the HTTP/2 in the plain connection, this is still experimental.

v0.3
====

> Date: 2018.06.18

The first release.


