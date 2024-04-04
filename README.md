# MindCheese

Portable Mindmap library written in TypeScript.

- Written in TypeScript
  - easy to maintain

Here's a demo site: https://tokuhirom.github.io/mindcheese/index.html

## **Note**

- This library based on jsMind: https://github.com/hizzgdev/jsmind
  - base commit hash is 33ad14832661034dc9a5a84bc0b0f18c93ceca4a

自分でビルドしたら試せます。

## Synopsis

```javascript
const container = document.getElementById("container");
const mindCheese = new MindCheese(container);
mindCheese.showNodeTree({
  id: "root",
  topic: "mindCheese",
  children: [
    {
      id: "easy",
      topic: "Easy",
      direction: "left",
      children: [
        { id: "easy1", topic: "Easy to show" },
        { id: "easy2", topic: "Easy to edit" },
        { id: "easy3", topic: "Easy to store" },
        { id: "easy4", topic: "Easy to embed" },
      ],
    },
    {
      id: "open",
      topic: "Open Source",
      direction: "right",
      children: [
        { id: "open1", topic: "on GitHub" },
        { id: "open2", topic: "BSD License" },
      ],
    },
    {
      id: "powerful",
      topic: "Powerful",
      direction: "right",
      children: [
        { id: "powerful1", topic: "Base on **TypeScript**" },
        {
          id: "powerful2",
          topic: "Base on **jsMind**",
          children: [{ id: "jsMind1", topic: "Base on HTML5" }],
        },
        { id: "powerful4", topic: "Depends on you" },
      ],
    },
    {
      id: "other",
      topic: "test node",
      direction: "left",
      children: [
        { id: "other1", topic: "I'm from local variable" },
        { id: "other2", topic: "I can do everything: `3*2`" },
      ],
    },
  ],
});
```

## Motivation

jsMind is a great library to implement the mindmap editor.
... and so, I want to add/modify some features. But jsMind is written in pure javascript.
Large library written in pure JavaScript is hard to modify.
As a result, I port whole of the jsMind to TypeScript. And I added some features, what I want.

### Difference between original jsmind

- Ported to TypeScript.
- Better look and feel

## Hacking

    npm run dev

## Keyboard shortcuts

Please look at [ShortuctOption](https://github.com/tokuhirom/mindcheese/blob/main/src/mindmap/MindOption.ts#L32-L45)

## How to release new version

- Create new git tag.
- Create release on github site.
- Github actions released new version to npmjs.org.

## FAQ

### How do I input multiple lines in the node?

You can type Shift+Enter.

## LICENSE

MindCheese modified part is licensed by the MIT license.

    The MIT License (MIT)

    Copyright © 2022 Tokuhiro Matsuno, http://64p.org/ <tokuhirom@gmail.com>

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the “Software”), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN

And this library is based on jsMind. Here's a license of jsMind.

    Copyright (c) 2014-2021, ZHANG ZHIGANG <hizzgdev@163.com>
    All rights reserved.

    Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

    * Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
    * Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
    * Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.


    版权所有 (c) 2014-2021, 张志刚 <hizzgdev@163.com>
    保留一切权利。

    在满足下列条件的前提下，授予使用者使用及再发布本软件的源代码或二进制形式的权利，无论是否修改皆然：

    * 对于本软件源代码的再发布，必须保留上述的版权声明、此三条许可条件，以及下述的免责声明。
    * 对于本软件二进制形式的再发布，必须在随同提供的文档和/或其它媒介中，包含上述的版权声明、此三条许可条件，以及下述的免责声明。
    * 未获得事前书面许可，不得使用版权所有人的名称和贡献者的名字，来为本软件的衍生物做任何支持、认可或推广、促销的行为。

    此软件由版权所有者及贡献者以现状（"as is"）方式提供，本软件不负任何明示或暗示的担保责任，包括但不限于就适销性以及特定目的的适用性的暗示性担保。任何因使用本软件造成的，直接、间接、连带、特别、惩戒或任何结果的损害（包括但不限于替代商品及服务的采购，无法使用，数据丢失，盈利损失或业务中断等），无论任何条件、无论任何原因或任何责任推断、无论是否属于合同范畴、无论是否为严格赔偿责任或民事侵权行为（包括过失或其他原因）而起，即使在使用前已获告知可能会造成此类损害的情形下，版权所有者及贡献者均不负任何责任。
