## tampermonkey-template

一个油猴脚本模板，参考 https://github.com/kinyaying/wokoo 开发。

将代码复制到油猴脚本，后在本地进行开发，开发完成之然后用 `app.bundle.js` 文件替换文本

```js
// ==UserScript==
// @name         Tampermonkey Nmae
// @namespace    https://github.dev/zishume/tampermonkey
// @version      0.0.1
// @description  Tampermonkey description
// @author       zishume
// @match        http://*/*
// @match        https://*/*
// @icon         https://www.google.com/chrome/static/images/chrome-logo-m100.svg
// @require      https://cdn.bootcss.com/jquery/3.6.0/jquery.min.js
// @grant        none
// @license MIT
// ==/UserScript==

(function() {
  'use strict';
  
  // 替换
  if(location.href === "http://localhost:8080/") return
  let script = document.createElement('script')
  script.src='http://localhost:8080/app.bundle.js'
  document.body.appendChild(script)
  // 替换

})();
```

## 开发脚本

- [https://greasyfork.org/zh-CN/scripts/453411-全局摸鱼看掘金沸点](https://greasyfork.org/zh-CN/scripts/453411-%E5%85%A8%E5%B1%80%E6%91%B8%E9%B1%BC%E7%9C%8B%E6%8E%98%E9%87%91%E6%B2%B8%E7%82%B9/code)
- [https://greasyfork.org/zh-CN/scripts/454963-v2ex图片灯箱插件](https://greasyfork.org/zh-CN/scripts/454963-v2ex%E5%9B%BE%E7%89%87%E7%81%AF%E7%AE%B1%E6%8F%92%E4%BB%B6/code)

