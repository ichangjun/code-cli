<!--
 * @Author: changjun anson1992@163.com
 * @Date: 2024-04-12 14:39:32
 * @LastEditors: changjun anson1992@163.com
 * @LastEditTime: 2024-04-12 15:50:55
 * @FilePath: /CODE-CLI/README.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->

# CODE-CLI 脚手架工具工程的搭建步骤

## 1. npm init -y 执行初始化，并添加 bin 脚本执行命令

npm i 简单，省略该步骤，直接执行 bin 脚本命令即可。

```json
{
  "name": "code-cli",
  "version": "2.0.0",
  "description": "code template cli",
  "main": "app.js",
  "bin": {
    "code-cli": "./bin/cli.js"
  }
}
```

完成这一步，如果我们想要在 cmd 中执行 `code-cli` 命令，我们需要在全局环境中安装 `code-cli` 包。

执行 npm link，将当前项目链接到全局环境。

```bash
npm link
# 结果如下，表示已经成功
# changed 1 package, and audited 3 packages in 3s
```

## 2. 创建 bin 目录及 cli.js 文件

```bash
mkdir bin && touch bin/cli.js
```

## 3. 编写 cli.js 脚本

```js
#! /usr/bin/env node
// 这个注释很重要，它告诉系统使用哪个解释器来执行这个脚本。
// 这里使用了 Node.js 解释器。
console.log('Hello World!')
```

## 4. 执行 cli.js 脚本

```bash
code-cli
# 结果如下，表示成功输出 Hello World!
# Hello World!
```
