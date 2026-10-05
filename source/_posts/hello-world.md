---
title: Hello World
tags: greeting
---
Welcome to [Hexo](https://hexo.io/)! This is my very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)



# Hexo + Fluid 功能集中演示

> 这是一篇用于测试 Hexo + Fluid 各种写作功能的 Demo。

---

## 1. Note

### Info

{% note info %}
这是一个 `info` note。

可以在这里写 **Markdown**，也可以写数学公式：
{% endnote %}

### Success

{% note success %}
证明已经完成。
{% endnote %}

### Warning

{% note warning %}
这里需要特别注意：这个假设不能被删除。
{% endnote %}

### Danger

{% note danger %}
如果忽略这个条件，结论一般不成立。
{% endnote %}

### Primary

{% note primary %}
这是 `primary` 类型的提示框。
{% endnote %}

### Secondary

{% note secondary %}
这是 `secondary` 类型的提示框。
{% endnote %}

---

## 2. Tabs

Tabs 非常适合展示不同情况。

{% tabs geometry %}

<!-- tab Closed surface -->

设 $S$ 是一个闭的双曲曲面。


<!-- endtab -->

<!-- tab Cusp -->

如果存在 cusp，则相应的端是抛物型的。

<!-- endtab -->

<!-- tab Funnel -->

如果存在 funnel，则相应的端是双曲型的。

<!-- endtab -->

{% endtabs %}

---

## 3. Fold

Fold 最适合隐藏较长的证明或者技术细节。

{% fold info @Proof %}

我们证明：

由基本积分公式，


{% endfold %}

### Technical details

{% fold secondary @Technical details %}

这里可以放比较冗长的计算，而不会让正文显得过于拥挤。

例如：

{% endfold %}

---

## 4. Label

Label 适合在正文中标记关键词。

{% label primary @Definition %}

{% label info @Important %}

{% label success @New %}

{% label warning @Warning %}

{% label danger @Danger %}

例如：

The {% label info @earthquake measure %} plays an important role in the theory.

---

## 5. Blockquote

可以使用 Hexo 的 blockquote Tag。

{% blockquote Henri Poincaré %}
这里放一段引用。
{% endblockquote %}

也可以把它用于数学史背景。

{% blockquote Thurston %}
这里可以放 Thurston 的相关引用。
{% endblockquote %}

---

## 6. Post Link

如果博客中有另一篇文章，例如：


可以使用：

```text
{% post_link earthquake %}
```

或者指定显示名称：

```text
{% post_link earthquake 'Earthquake Theory' %}
```

实际使用时：

See also ```{% post_link earthquake 'Earthquake Theory' %}```.

> 如果你的博客里不存在 `earthquake.md`，这个链接当然需要替换成你实际存在的文章。

---

## 7. Include Code

假设目录中有：

```text
source/
├── _posts/
│   └── hexo-demo.md
└── _data/
    └── example.py
```

可以使用：

```text
{% include_code lang:python example.py %}
```

例如：

{% include_code lang:python example.py %}

也可以只引入某一部分代码，例如：

```text
{% include_code lang:python from:10 to:20 example.py %}
```

这对于展示实验代码非常有用。

---

## 8. Raw

如果我们希望**展示 Hexo Tag 本身，而不是让 Hexo 执行它**，可以使用 `raw`。

例如：

{% raw %}

```text
{% note warning %}
This is an example.
{% endnote %}
```

{% endraw %}

上面的内容会作为普通文本展示，而不会真的生成 Note。

这在写 Hexo 教程时尤其有用。

---

## 9. Markdown Code Block

普通 Markdown 代码块：

```python
import numpy as np

x = np.linspace(0, 1, 100)

y = x ** 2

print(y)
```

也可以展示其他语言：

```julia
function f(x)
    return x^2
end
```

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, Hexo!";
    return 0;
}
```

## 11. Image

普通 Markdown：

```markdown
![Example image](/img/example.png)
```

也可以使用 Hexo 的图片 Tag：

```text
{% img /img/example.png 600 400 %}
```

例如：

{% img /img/example.png 600 400 %}

> 如果你的 `/img/example.png` 不存在，这里需要替换成实际图片路径。

---

## 12. TOC

对于较长文章，可以根据标题自动生成目录。

例如本文包含：

- Note
- Tabs
- Fold
- Label
- Blockquote
- Post Link
- Include Code
- Raw
- Code Block
- Mathematical Formula
- Image

可以在文章开头或者适当位置放置目录。

如果你的 Fluid 配置启用了 TOC，可以利用文章标题自动生成导航。

---

## 13. 综合示例：数学定理

下面把前面的功能组合起来。

{% note info %}

**Theorem.** Let $(X,d)$ be a compact metric space. Then every continuous function

is bounded.

{% endnote %}

{% fold info @Proof %}

由于 $X$ 是紧空间，而 $f$ 连续，因此 $f(X)$ 是 $\mathbb R$ 中的紧集。

$\mathbb R$ 中的紧集是有界的，所以存在 $M>0$，使得


因此 $f$ 有界。

{% endfold %}

{% note success %}

**Conclusion.** Compactness + continuity gives boundedness.

{% endnote %}

---

## 14. 综合示例：Case Distinction

{% tabs cases %}

<!-- tab Case 1: Compact -->

{% note info %}
$X$ 是紧的。
{% endnote %}

由紧性可以获得有限覆盖等性质。

<!-- endtab -->

<!-- tab Case 2: Locally compact -->

{% note warning %}
局部紧性只给出局部性质，不能直接替代全局紧性。
{% endnote %}

<!-- endtab -->

<!-- tab Case 3: Non-compact -->

{% note danger %}
如果 $X$ 非紧，则连续函数不一定有界。
{% endnote %}

<!-- endtab -->

{% endtabs %}

---

## 15. 综合示例：Research Note

{% label primary @Idea %}

考虑一个研究问题：


{% note warning %}

**Potential problem.**

原来的证明使用了 compactness，但实际上可能只需要 properness。

{% endnote %}

{% fold secondary @Possible approach %}

第一步，检查证明中 compactness 第一次出现的位置。

第二步，判断那里实际上使用的是：


第三步，尝试用 properness 替代。

{% endfold %}

{% note success %}

**Research direction.**

如果替换成功，可能得到一个更一般的 theorem。

{% endnote %}

---

## 16. Checkbox

可以把它作为 Research TODO：

{% cb Read the original paper %}

{% cb Check the proof %}

{% cb Find a counterexample %}

{% cb Write the generalization %}

也可以默认勾选：

{% cb First step completed, true %}

---

# 17. 一个完整的数学笔记模板

以后写数学研究笔记，可以直接采用下面的结构：

{% note info %}

**Definition.**

定义研究对象。

{% endnote %}

{% note primary %}

**Main Question.**

我们真正想解决的问题是什么？

{% endnote %}

{% note success %}

**Main Idea.**

核心思路是什么？

{% endnote %}

{% tabs approaches %}

<!-- tab Approach A -->

第一种方法$X$。

<!-- endtab -->

<!-- tab Approach B -->

第二种方法。

<!-- endtab -->

{% endtabs %}

{% note warning %}

**Technical obstacle.**

目前真正困难的地方。

{% endnote %}

{% fold info @Proof / Calculation %}

详细证明或者计算。

{% endfold %}

{% fold secondary @Further questions %}

这里记录证明完成以后产生的新问题。

{% endfold %}

{% cb Check references %}

{% cb Write proof %}

{% cb Run numerical experiment %}

---

# 18. 最终总结

本文集中演示了：

{% label primary @Note %}
{% label primary @Tabs %}
{% label primary @Fold %}
{% label primary @Label %}
{% label primary @Post Link %}
{% label primary @Blockquote %}
{% label primary @Include Code %}
{% label primary @Raw %}
{% label primary @Code Block %}
{% label primary @Math %}
{% label primary @Image %}
{% label primary @TOC %}
{% label primary @Checkbox %}

其中，对于数学研究博客，我最推荐的组合是：


它们分别负责：

| 功能 | 用途 |
|---|---|
| Note | 定义、定理、警告、重要观点 |
| Tabs | 不同情况、不同证明、不同方法 |
| Fold | Proof、Technical Details |
| Label | Definition、Idea、Important 等标签 |
| Post Link | 建立文章之间的知识网络 |
| Blockquote | 文献与历史背景 |
| Include Code | 实验代码 |
| Raw | 展示 Hexo 语法 |
| Checkbox | Research TODO |
| MathJax | 数学公式 |
| Image | 几何图、示意图 |
| TOC | 长文章导航 |
