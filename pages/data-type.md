---
layout: section
---

# 資料型態

## 與他們的產地

---

# 什麼是資料型態？

::v-clicks{depth=2}
* 就是指[資料的種類]{v-mark.underline.red="1"}。
* 通常種類分為:
    :::ul{.pl-20}
    * 文字
    * 整數
    * 浮點數
    * 布林值
    * etc.{.font-mono}
    :::
* [Python]{.font-mono} 還有其他的類型，如 [list]{.font-mono}、[dict]{.font-mono}、[bytes]{.font-mono} 等。
::

---

# 資料為什麼分型態？

記得「宣告 [Declare]{.font-mono}」和「賦值 [Assignment]{.font-mono}」嗎？

::grid-block {classNames="pt-4 pb-12 px-6" v-click="1"}
:::div{.bg-green-200 .rounded-l-lg .p-4}
宣告 {.text-3xl .font-bold}

跟電腦請求記憶體空間，準備存放資料。{.px-6 .pt-5 v-click="2"}
:::
:::div{.bg-yellow-200 .rounded-r-lg .p-4}
賦值 {.text-3xl .font-bold}

將資料（值）放到記憶體空間中。{.px-6 .pt-5 v-click="3"}
:::
::

---

# 資料為什麼分型態？（續）

::center-flex-block
:::div{.text-4xl .pb-6}
宣告時，要開多大的記憶體空間給資料？
:::
:::p{.text-5xl .pb-6 v-click}
就是由「[資料型態]{v-mark.underline.red="1"}」來決定！
:::
::

---

# 補充：不同程式語言對資料型態

::grid-block{classNames="p-5"}
:::div{.px-2 v-click}
強型別{.text-center .text-3xl .font-bold}

宣告時，需要提前告訴電腦你即將儲存的資料是什麼類型。{.pt-3 style="text-indent: 2em;"}
:::
:::div{.border-black .border-l-2 .px-2 v-click}
弱型別{.text-center .text-3xl .font-bold}

宣告時，不用特別先告訴電腦你要存放的資料類型，電腦會先給你一段超大的空間，讓你後續方便儲存各種類型的資料。{.pt-3 style="text-indent: 2em;"}
:::
::

---

# 如何檢查是什麼資料型態？

::div{.text-3xl .pl-4 .pt-4 v-click}
可以利用 `type()`{.font-mono} 方法來進行檢測。 
::

::div{.font-mono .px-6 .pt-4 v-click}
```py {monaco-run} {autorun: false, lineNumbers: 'on', height: '10rem', editorOptions: { fontSize: 16 } }
print("文字型別:", type("abc"))
print("整數型別:", type(123))
print("布林值型別:", type(True))
print("List 型別:", type([1,2,3]))
print("Dict 型別:", type({"a": 1, "b": 2, "c": 3}))
print("Bytes 型別:", type(b"abc"))
```
::

---

# 補充：比對資料型態

::div{.text-3xl .pl-4 .pt-4 v-click}
如果要比對某個資料是不是某種資料型態，可以使用內建函式 `isinstance()`{.font-mono} 來檢查。
::

::div{.font-mono .px-6 .pt-4 v-click}
```py {monaco-run} {autorun: false, lineNumbers: 'on', height: '10rem', editorOptions: { fontSize: 16 } }
# 檢查是否為數字型態
# isinstance(待測資料, 待測資料型態)

print("123 是否為整數型態？", isinstance(123, int))
print("'abc' 是否為整數型態？", isinstance('abc', int))
```
::

---

# RECAP{.font-mono}

::v-clicks{depth="2"}
* 資料型態是指資料的種類。
* 不同資料型態，所需要的記憶體儲存空間不同。
* [Python]{.font-mono} 是一種弱型別的程式語言。
    * 也就是說：[不用]{v-mark.circle.red="4"}提前**宣告**{.text-4xl .text-rose-600 .underline .underline-offset-6}電腦現在要存什麼型態的資料。
* 在 [Python]{.font-mono} 中可以使用 `type(data)`{.font-mono} 來查看資料的型別。
::