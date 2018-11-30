## 如何使用

安装Carlo

#### npm

```
npm i carlo
# yarn add carlo
```

> Carlo 需要Node的版本至少为v7.6.0。

**示例**

* 展示本地环境

将以下内容保存为**example.js**文件

```js
const carlo = require('carlo');

(async () => {
  // Launch the browser.
  const app = await carlo.launch();

  // Terminate Node.js process on app window closing.
  app.on('exit', () => process.exit());

  // Tell carlo where your web files are located.
  app.serveFolder(__dirname);

  // Expose 'env' function in the web environment.
  await app.exposeFunction('env', _ => process.env);

  // Navigate to the main page of your app.
  await app.load('example.html');
})();
```

将以下内容保存为**example.html**文件

```html
<script>
async function run() {
  // Call the function that was exposed in Node.
  const data = await env();
  for (const type in data) {
    const div = document.createElement('div');
    div.textContent = `${type}: ${data[type]}`;
    document.body.appendChild(div);
  }
}
</script>
<body onload="run()">
```

运行你的应用:

```bash
node example.js
```

查看拥有更加丰富的UI和基于Web和Node之间远程调用通信的例子在 \[examples\]\([https://github.com/GoogleChromeLabs/carlo/tree/master/examples\](https://github.com/GoogleChromeLabs/carlo/tree/master/examples\)\) 目录

