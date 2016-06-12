Atom 大家应该都不陌生, 是 Github 出的基于 electron 框架开发的的编辑器, 这里就不详细介绍了. 今天要说的是 Nuclide, Nuclide 是一款由facebook开发,基于atom的,针对 web/mobile 开发定制的 IDE, 并且支持 React/ReactNative开发。

Mac 上的安装

1、因为上面说了Nuclide是基于Atom开发, 所以首先要在 https://atom.io/ 下载并安装Atom .

2、使用 apm install nuclide 安装 Nuclide

如果提示 apm 命令不存在, 可以打开 Atom 然后点击菜单栏的 Atom, 在下拉菜单里面选择 Install Shell Commands

3、安装好以后打开 Atom, 选择 Atom - Preferences - Packages - Nuclide, 然后勾选 Install Recommended Packages on Startup, 如下图:

2016-03-30_1459268133958943348.png

这一步主要是安装如下工具包

1
2
3
4
5
tool-bar to enable the Nuclide toolbar.
sort-lines to enable sorting lines of text.
language-ocaml to enable OCaml language syntax highlighting.
language-babel to enable language grammar for JS, Flow and React JS, etc.
...
4、安装其它 Atom 包

1
2
terminal-plus: 集成命令行
linter-eslint: JS语法检查
5、全局安装eslint, 并生成配置文件.eslintrc.json。

1
2
npm install eslint -g
eslint --init
我的配置文件如下:

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es6": true,
        "node": true
    },
    "extends": "eslint:recommended",
    "parserOptions": {
        "ecmaFeatures": {
            "experimentalObjectRestSpread": true,
            "jsx": true
        },
        "sourceType": "module"
    },
    "plugins": [
        "react",
        "react-native"
    ],
    "ecmaFeatures": {
      "jsx": true
    },
    "rules": {
        "indent": [
          2,
          "tab"
        ],
        "linebreak-style": [
            "error",
            "unix"
        ],
        "quotes": [
            "error",
            "single"
        ],
        "semi": [
            "error",
            "always"
        ],
        "react-native/no-unused-styles": 2,
        "react-native/split-platform-components": 2
    }
}
6、安装 eslint 插件

1
npm install --save-dev babel-eslint eslint-plugin-react eslint-plugin-react-native
效果如下: