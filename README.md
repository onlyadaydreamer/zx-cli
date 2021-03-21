<!--
 * @file: description
 * @author: zhangxing
 * @Date: 2020-08-23 20:35:34
 * @LastEditors: zhangxing
 * @LastEditTime: 2020-09-09 11:28:38
-->

1. 创建可执行的脚本

下面这一句必须的

```bash
#! /usr/bin/env node 使用全局环境中安装的 node
```

2. 配置 package.json 中的 bin 字段
3. npm link 链接到全局

```

/usr/local/bin/zx-cli -> /usr/local/lib/node_modules/zx-cli/bin/zx
/usr/local/lib/node_modules/zx-cli -> /Users/zhangxing/Desktop/zx-cli
```

注意最终使用的命令是和 package.json 中的 name 属性一致

也可以使用其他名字

```js
"bin": {
  "zx": "./bin/zx",
  "zx-cli": "./bind/zx"
}
```

这样我们就可以通过执行 `zx --help`来查看所有命令了

4. 主要使用的包
