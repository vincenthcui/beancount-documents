## 开始使用 Beancount

### 介绍

本文档将会引导你创建第一个 beancound 文件，初始化选项。我们还会介绍如何组织你的文件目录，如何声明账户，并确保他们的初始金额是正确无误的。如果你使用 Emacs，我们也提供了一些配置文件编辑器的建议。

在阅读本文档前，建议先浏览[用户手册](http://furius.ca/beancount/doc/users-manual)熟悉beancount语法和指令。如果你已经配置过beancount文件，可以继续查阅[语法手册](http://furius.ca/beancount/doc/cookbook)。如果你是 Ledger 用户，可以先研究 [Ledger 和 beancount 的不同](http://furius.ca/beancount/doc/comparison)。

### 编辑器支持

#### Emacs

在编辑 beancount 文件的时候，你想要文件编辑器更好的支持 beancount 语法。我会介绍我配置 Emacs 的经验，当然，你可以用其他你熟悉的编辑器操作。

#### Vim

Nanthan Grigg 实现了 Vim 插件，代码托管在 [Github](https://github.com/nathangrigg/vim-beancount)，支持以下特性：

1. 语法高亮（不够详细，但是基本的都支持）
2. 账户名称补齐
3. 在账单中对齐小数点

#### Sublime

Martin Andreas Andersen 提供了 Sublime 的支持，具体查看[代码仓库](https://github.com/draug3n/sublime-beancount)

### 创建第一个账单文件

我们创建一个最小的账单文件，它拥有两个账户和一条账单。输入或者复制下面的的文字到文本文件里

```beancount
2014-01-01 open Assets:Checking
2014-01-01 open Equity:Opening-Balances

2014-01-02 * "Deposit"
  Assets:Checking           100.00 USD
  Equity:Opening-Balances
```

### 简单回顾下语法

简短的笔记和特别简单 beancount 语法回顾：

- 货币标记必须全部大写（允许数字和特殊符号 `_`、`-`），不支持货币符号（`$`，`€`）
- 