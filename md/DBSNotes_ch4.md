# 資料庫系統筆記 Ch. 4

> 參考書籍：
>
> 1. 《Databases System 7th Edition》─ Ramez Elmasri, Shamkant B. Navathe.
> 2. 《數據庫系統基礎 第六版》─ Ramez Elmasri, Shamkant B. Navathe，李翔鷹、劉鑌、邱海艷、陳立軍譯
>
> 筆記作者：[黃漢軒](https://ntut-xuan.github.io)



## EER 模型

除了本身的 ER 模型之外，還多了：

- 子類別（Subclass）、父類別（Superclass）。
- 特別化（Specialization）、一般化（Generalization）。
- 類別（Category）、並類別（Union type）。
- 屬性（Attribute）、關聯繼承（Relationship Inheritance）的重要機制。

新增了這些東西的 ER 模型，稱為 EER 模型（Enhanced-ER model）。



## 子類別、父類別與繼承

### 定義子類別與父類別

- 子類別（Subclass），即把一個實體類型，分成多個有意義的分組或子類別，被分的實體類型就稱為父類別（superclass），例如：
- 對於一間公司來說，`EMPLOYEE` 可能同時也可以分成 `SECRETARY`、`MANAGER` 等。
- 在這邊的 `SECRETARY` 與 `MANAGER` 就是子類別。
- 在這邊的 `EMPLOYEE` 就是父類別。

> TODO：補圖



### 子類別與父類別的一些特性

- 對於子類別與父類別的關聯，就稱為「父類別／子類別關聯」（Superclass/subclass Relationship），同時也可以稱為「父類型／子類型關聯」（Supertype/subtype Relationship），也可簡稱為「類別／子類別關聯」（Class/subclass Relationship）。
- 子類別中的實體必須同時為父類別的實體，例如：秘書（`SECRETARY`）必須同時也是員工（`EMPLOYEE`）的實體，秘書的實體不能獨立存在，必須要是以父類別，也就是員工實體的一部分，來分出子類別實體。

> TODO：補圖



### 類型繼承的特性

- 對於從父類別與子類別，他們是從父類別中被分出了各式各樣的子類別。
- 因此子類別應該要有父類別的所有屬性，以及子類別自己本身的一些屬性，如同繼承的概念。
- 若這些子類別除了從父類別繼承的一些屬性之外，也有自己的屬性，那這個子類別也應該被當成一種實體類別。



## 特殊化與一般化

### 特殊化

- 對於一個父類別被分成子類別的這個動作，稱為特殊化。
- 例如：將員工（`EMPLOYEE`）分為秘書（`SECRETARY`）、工程師（`ENGINEER`）等等，這個動作稱為特殊化。
- 特殊化後，每個子類別可以擁有自己的屬性，或者擁有自己的關聯類型。
  - 若子類別擁有自己的屬性，這些屬性稱為專有屬性（Specific Attribute）。
  - 若子類別擁有自己的關聯類型，這些關聯類型稱為專有關聯類型（Specific Relationship）。
- 特殊化將父類別與子類別使用圓圈進行連接，圓圈與子類別具有一符號，描述是從哪個父類別被分出了子類別。

> TODO：補圖



### 一般化

- 若今天有兩個類似的實體類型，例如汽車與卡車，我們可以使用一般化，來提取他們的共同屬性。
- 概念上即為特殊化的逆向過程，我們可以利用這樣的方式，來讓兩個屬性使用一個屬性來當作父類別，簡潔 EER Diagram。

> TODO：補圖