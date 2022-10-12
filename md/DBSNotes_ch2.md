# 資料庫系統筆記 Ch. 2

> 參考書籍：
>
> 筆記作者：[黃漢軒](https://ntut-xuan.github.io)



## 資料庫模型、模式與狀態

### 資料庫模型

- 主要可以分成三種不同類型的資料庫模型：
  - 高層 - 概念資料庫模型（Conceptual Data Model）
  - 低層 - 物理資料庫模型（Physical Data Model）
  - 介於高層與低層之間 - 表示資料庫模型（Representation Data Model）
    - 在資料庫中最常被使用，因為不會因為過於概念而拋棄底層概念，也不會因為過於底層而難以理解。
    - 包含了過時的網狀模型（Network Model）與層次模型（Hierarchical Model）。
- 在模型中可以看到以下的概念：
  - 實體（Entity）：泛指真實世界中的對象或概念。
  - 屬性（Attribute）：泛指真實世界中某個感興趣的特性。
  - 關聯（Relationship)：泛指實體之間的關聯。



### 資料庫模式

- 對於資料庫來說，資料庫模式（Database Schema）泛指對於資料庫的描述。
- 資料庫模式*一般認定上*並不會被頻繁的改變，它會在規劃資料庫時進行設計，在未來進行微調。
  - 通常伴隨著需求的改變，會導致資料庫會有所改變，稱為模式演化（Schema Evolution）。

- 在描述資料庫中所有表格的圖，我們稱為模式圖（Schema Diagram）

  - 絕大多數情況下，資料庫所有表格都可以呈現出模式圖，如下圖即呈現了一個資料庫中的模式圖。

  - 裡面的資料表格稱為模式構件（Schema Constructor），透過多個模式構件可以產生出模式圖。

    <img src="/home/xuan/.config/Typora/typora-user-images/image-20221012155424626.png" alt="image-20221012155424626" style="zoom:50%;" />



### 資料庫狀態

- 資料庫的資料被稱為一個資料庫狀態（Databases State），或者可以稱為快照（Snapshot）。
- 資料庫狀態，即為資料庫中當前的具體值（Occurrence）或實例（Instance）的集合。
- 在初始灌檔進入資料庫時，資料庫即有第一次版本的資料狀態，稱為初始狀態。
  - 在之後的變更後每次都會產生一個資料狀態，即為版本上的變換。
  - 資料庫會確保每一次的資料狀態都是有效的，保證有效狀態（Valid State）。