---
layout: section
---

# 文字型別資料

## 各種常用

---

# 文字型別資料有哪些？

::v-clicks
:::ul{.pt-4 .pl-20}
* 字元 （[Character]{.font-mono}，[chr]{.font-mono}）
* 字串 （[String]{.font-mono}，[str]{.font-mono}）
:::
::

::div{.text-center .text-4xl .mt-10 v-click}
在 [Python]{.font-mono} 中，平常都只用到 [String]{.font-mono} 。
::

---

# 字串：頻繁用到的型態

::div{.text-3xl .pt-4 .px-8 style="text-indent: 2em;"}
正如你所知道的，我們利用 `""`{.font-mono} 或 `''`{.font-mono} 包起來後的資料，就是**字串**資料。
::

::div{.font-mono .px-6 .pt-4 v-click}
```py {monaco-run} {autorun: false, lineNumbers: 'on', height: '10rem', editorOptions: { fontSize: 16 } }
# 請你在這邊用 type 檢驗變數 `variable` 中儲存的資料型態。
variable = "1234"
```
::

---

::center-flex-block{classNames="pb-12 gap-6"}
那字元呢？{.text-4xl}

:::div{.text-3xl v-click}
恩... [Python]{.font-mono} 中[沒有]{.text-4xl .text-rose-600 .underline .underline-offset-4}字元這個型態。
:::
:::div{.text-2xl v-click}
但有一個神奇的內建函式 `chr()`{.font-mono} 可以[將數字依照 ASCII 編碼變成文字]{v-mark.underline.red="2"}。
:::
::

---

# 字串的 [２３]{.font-mono} 事

在 [Python 3]{.font-mono} 中， `input()`{.font-mono} 進來的資料都是**字串**。

::div{.font-mono .px-6 .pt-4}
```py {monaco-run} {autorun: false, lineNumbers: 'on', height: '10rem', editorOptions: { fontSize: 16 } }
# 請你在這邊用 type() 驗證 input() 的資料為字串型態。
# stdin: 這是一個字串
variable = input()
```
::

---

# 字串的一些功能

::v-clicks
* `str.upper()`{.font-mono}：全部變成大寫 
* `str.lower()`{.font-mono}：全部變成小寫 
* `str.capitalize()`{.font-mono}：第一個英文字母變大寫 
* `str.isdigit()`{.font-mono}：檢查是否為字串是否都是數字 
* `str.split()`{.font-mono}：將特定字元作為切分點，把字串切開變成 [list]{.font-mono} 
* `str.join()`{.font-mono}：將 `str`{.font-mono} 作為連接的字，把 `join` 後括號中的 `str list`{.font-mono} 資料串起來變成一個字串。
::