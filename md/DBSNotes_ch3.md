# 資料庫系統筆記 Ch. 3

> 參考書籍：
>
> 1. 《Databases System 7th Edition》─ Ramez Elmasri, Shamkant B. Navathe.
> 2. 《數據庫系統基礎 第六版》─ Ramez Elmasri, Shamkant B. Navathe，李翔鷹、劉鑌、邱海艷、陳立軍譯
>
> 筆記作者：[黃漢軒](https://ntut-xuan.github.io)



## 使用高階概念資料模型來進行資料庫規劃

下圖為簡化的資料庫設計概念：

- 先從一些特定主題的集合（Miniworld）開始，進行「需求集合與分析」（Requirements collection and analysis）。
- 有了函數需求（Functional Analysis）之後就能夠進入函數分析（Functional Analysis）
- 有了資料需求（Data Requirements）之後就能夠進入概念設計（Conceptual Design）
  - 從概念設計取得概念模式（Conceptual Schema），在這邊會得到 ER Diagram。
  - 從概念模式取得邏輯設計，得到邏輯模式（Logical Schema）。
  - 接著硬體設計並得到內層模式（Internal Schema）。

<img src="https://i.imgur.com/VpZsSj1.png" alt="image-20221020082217748" style="zoom: 67%;" />



## 實體關係模型與實體關係圖

我們使用實體關係圖（Entity Relational Diagram, ER Diagram），

來描述我們的實體關係模型（Entity Relational Model, ER Model），如下圖。

實體關係模型（ER Model）通常拿來描述概念資料模型（Conceptual Model），用來在特定系統中定義實體與關係。

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/72/ER_Diagram_MMORPG.png/1024px-ER_Diagram_MMORPG.png" alt="img" style="zoom: 50%;" />



## 實體類別、實體集、屬性與鍵

- 定義實體
  - 通常泛指一個獨立存在於現實生活中的事件或物件。
    - 現實生活中的物件，通常是物理上的存在，例如：學生、教授...
    - 現實生活中的事件，通常是概念上的存在，例如：課程、工作...
  - 實體具有多個屬性，例如學生具有名稱、學號等等。
    - 屬性又可詳細分成了以下七種不同的屬性：
      - 單值 vs 多值：
        - 單值屬性（Simple Attribute）：只有一個值，例如學號。
        - 多值數性（Multivalued Attribute）：用來儲存兩種以上的值的屬性，例如汽車的顏色。
      - 單元 vs 複合
        - 單元屬性（Atomic Attribute）：單一一種屬性，不可再切割，例如鄉鎮市區。
        - 複合屬性（Composite Attribute）：由兩個以上的屬性所組成，例如地址。
      - 儲存 vs 衍生
        - 儲存屬性（Stored Attribute）：可藉由衍生屬性進行推論的資料，例如出生年月日。
        - 衍生屬性（Derived Attribute）：由某種方式推論而成，例如利用出生年月日來推論出年紀。
  - 每個屬性具有值，因此我們就能使用這樣的方式來定義實體。
- 實體型態與實體集
  - 實體型態即為一個具有相同屬性的實體集合。
    - 可以想像成學校內的學生具有相同屬性，學校內的課程具有相同屬性。
  - 在某特定時間內，選擇某特定實體型態得到一集合，稱為實體集或實體集合。
  - 實體型態會呈現在 ER Diagram 上，以一個正方形方格來呈現實體型態。



