---
title: hexo YAMLException
date: 2017-08-08 23:16:12
tags: hexo YAMLException
---
# Hexo YAMLException

`$ hexo g
INFO  Start processing
ERROR Process failed: _posts/xx.md
YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key at line 4, column 1:

    ^
    at generateError (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:162:10)
    at throwError (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:168:9)
    at readBlockMapping (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:1045:9)
    at composeNode (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:1331:12)
    at readDocument (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:1493:3)
    at loadDocuments (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:1549:5)
    at Object.load (D:\blogs\Hexo\hexo-blog\node_modules\js-yaml\lib\js-yaml\loader.js:1566:19)
    at parseYAML (D:\blogs\Hexo\hexo-blog\node_modules\hexo-front-matter\lib\front_matter.js:80:21)
    at parse (D:\blogs\Hexo\hexo-blog\node_modules\hexo-front-matter\lib\front_matter.js:56:12)
    at D:\blogs\Hexo\hexo-blog\node_modules\hexo\lib\plugins\processor\post.js:52:18
    at tryCatcher (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\util.js:16:23)
    at Promise._settlePromiseFromHandler (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:509:35)
    at Promise._settlePromise (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:569:18)
    at Promise._settlePromise0 (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:693:18)
    at Promise._fulfill (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:638:18)
    at PromiseArray._resolve (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise_array.js:126:19)
    at PromiseArray._promiseFulfilled (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise_array.js:144:14)
    at PromiseArray._iterate (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise_array.js:114:31)
    at PromiseArray.init [as _init] (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise_array.js:78:10)
    at Promise._settlePromise (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:566:21)
    at Promise._settlePromise0 (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:614:10)
    at Promise._settlePromises (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:693:18)
    at Promise._fulfill (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:638:18)
    at PromiseArray._resolve (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise_array.js:126:19)
    at PromiseArray._promiseFulfilled (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise_array.js:144:14)
    at Promise._settlePromise (D:\blogs\Hexo\hexo-blog\node_modules\bluebird\js\release\promise.js:574:26)
INFO  Files loaded in 832 ms
INFO  0 files generated in 952 ms
`
###解决思路
1. 检查主目录下配置文件_config.yml里Site和Url所有属性:后面是否全部有一个空格;
2. 检查要渲染的md文件中的 title, date, tags的':'后面是否有一个空格,如果没有请添加一个空格;

本人就是在tags:后面没有添加一个空格...



