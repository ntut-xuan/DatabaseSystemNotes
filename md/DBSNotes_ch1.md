# 資料庫系統筆記 Ch.1



## 資料庫

### 資料庫類型

- 傳統應用類型
    - 數字與文字資料庫（Numeric and Textual）
- 近期發展類型
    - 多媒體資料庫
    - 地理資訊系統（Geographic Information System, GIS）
    - 生物與基因資料庫
    - 資料倉儲（Data Warehouses）
    - 行動資料庫
    - 即時資料庫（Real-time and Active）

社交網路（Social Network）大量的交流資訊、搜尋引擎蒐集網頁資訊等......大量資料管理，促進各種新技術發展：
- 大數據儲存系統（Big Data storage system）
    - 使用大量伺服器組成大型資料庫叢集。
- NOSQL Systems（Not Only SQL）


### 資料庫名詞的基本定義

- 資料庫：一群有關聯的資料的集合。
- 資料：可以被記錄，具有隱含意義的事實。
- 迷你世界（論域, Universe of discourse, UoD）：真實世界的一部分儲存在資料庫中。
- 資料庫管理系統（Database management system, DBMS）：可以管理資料庫的軟體，例如：MySQL、MariaDB、MS SQL ...
- 資料庫系統：由 DBMS 與資料組成，有時應用程式也包括在內。



### 資料庫的簡化圖

<img src="https://i.imgur.com/qNPN9TO.png" alt="image-20220922082924228" style="zoom: 67%;" />



### 資料庫管理系統功能

以典型的資料庫來舉例：
- 根據資料類型（Types）、結構（Structures）、限制（Constraints），定義特定資料庫。
- 在次要的儲存裝置，建構（Construct）或載入（Load）初始資料庫內容。
- 操作資料庫，例如：查詢、生成報告、插入、刪除、更新，能夠透過網路應用程式來存取。
- 由一組使用者和應用程式同時進行資料的處理與共享，但仍然保持資料的有效性與一致性。

### 資料庫管理系統額外功能

- 保護（Protection）功能，防止軟硬體故障或當機（Crashes）。
- 安全性（Security）功能，防止未經授權（Unauthorized）或惡意（Malicious）存取。
- 資料呈現（Presentation）與視覺化（Visualization）。
- 在資料庫應用程式的生命週期內，維護資料庫及相關程式。
- 呼叫資料庫、軟體及系統維護。

### 資料庫應用程式功能

- 查詢（Queries），查詢不同部分的資料，訂定請求的結果。
- 交易（Transactions），讀取一些資料並更新某些值，或是生成新資料並儲存於資料庫中。
- 不允許未經驗證的使用者存取資料。
- 必須滿足使用者對資料庫的需求變化。




### 資料庫的特性

- 自我描述性（Self-describing）
    - DBMS 目錄（Catalog）儲存特定資料庫的描述（Meta-data, 詮釋資料）。
        - 包含資料結構、類型與限制。
        - 部分新系統不需要詮釋資料。
    - 允許 DBMS 和不同的資料庫應用程式進行作業。
- 程式與資料間獨立
    - 允許修改資料結構與儲存方式，並無須修改 DBMS 存取程式。
- 資料抽象（Abstraction）化
- 支援資料 Multiple Views
- 共享資料和多使用者交易處理
> 待補

以趨近真實的資料庫來說明：



## 資料庫的使用者

主要分為使用資料庫的人與操作資料庫的人。

### 使用資料庫的人

在資料庫的管理上，主要可以分成三類人：

- 資料庫管理員（Database Administrators）：負責管理資料庫的人。
  - 負責在系統上運行資料庫、備份資料、規劃安全策略、保持資料庫的完整性。
- 資料庫設計者（Database Designer）：負責設計資料庫的人。
- 終端使用者（End User）：負責使用資料庫的人，可以細分成：
  - 非正式用戶（Casual End User）
  - 初級用戶（Naive User）
  - 高級用戶（Sophisticated User）
  - 獨行用戶（Standalone Users）：自建資料庫、自己用。



### 製造資料庫的人

- DBMS 設計師與開發人員
- 工具開發者
- 操作人員與維護人員：維護硬體設備。

