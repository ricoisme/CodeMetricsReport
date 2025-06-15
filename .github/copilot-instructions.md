
C# Coding Guideline

## 1. 一般設定

- 所有檔案使用 UTF-8 編碼。
- 使用 4 個空格作為縮排風格。
- 插入文件結尾的換行符。
- 移除行尾的空白字符。

## 2. 檔案副檔名設定

### 2.1 Visual Studio 解決方案檔案

- `.sln` 檔案使用 Tab 縮排。

### 2.2 Visual Studio XML 專案檔案

- `.csproj`, `.vbproj`, `.vcxproj.filters`, `.proj`, `.projitems`, `.shproj` 檔案使用 2 個空格縮排。

### 2.3 XML 配置檔案

- `.xml`, `.config`, `.props`, `.targets`, `.nuspec`, `.resx`, `.ruleset`, `.vsixmanifest`, `.vsct` 檔案使用 2 個空格縮排。

### 2.4 JSON 檔案

- `.json`, `.json5`, `.webmanifest` 檔案使用 2 個空格縮排。

### 2.5 YAML 檔案

- `.yml`, `.yaml` 檔案使用 2 個空格縮排。

### 2.6 Markdown 檔案

- `.md`, `.mdx` 檔案不會修剪行尾空白。

### 2.7 網頁檔案

- `.htm`, `.html`, `.js`, `.ts`, `.tsx`, `.css`, `.sass`, `.scss`, `.less`, `.vue` 等檔案使用 2 個空格縮排。

### 2.8 批次檔案

- `.cmd`, `.bat` 檔案使用 CRLF 進行行結束。

### 2.9 Bash 檔案

- `.sh` 檔案使用 LF 進行行結束。

### 2.10 Makefile

- `Makefile` 檔案使用 Tab 縮排。

## 3. .NET 程式碼風格嚴重性設定

- 預設所有 .NET 程式碼風格的診斷設定為 `warning`。

## 4. 語言規則

### 4.1 .NET 程式碼風格

- 取消 `this.` 和 `Me.` 的強制使用。
- 使用語言關鍵字替代框架類型。
- 強制使用訪問修飾符。
- 預設欄位為 `readonly`。
- 算數、邏輯和比較操作符總是用括號包裹。
- 推薦使用對象初始化器、集合初始化器。
- 支援空值傳播（`?.`）和合併運算子（`??`）。

### 4.2 C# 程式碼風格

- 鼓勵使用 `var`，尤其是在類型顯而易見時。
- 使用表達式主體的方法、屬性、構造函數等。
- 推薦使用模式匹配和 `switch` 表達式。
- 支援內嵌變數聲明。

### 4.3 無用程式碼規則

- 提醒並建議移除未使用的參數和變數。
- 移除不必要的賦值語句。

## 5. 格式化規則

- 強制 C# 程式碼塊中的每個 `if`, `else`, `catch`, `finally` 等語句前後有換行。
- 強制在每個語句和運算符之間有空格，並確保括號周圍沒有多餘的空格。

## 6. .NET 命名規則

### 6.1 一般命名規則

- 使用 PascalCase（大駝峰式）來命名命名空間、類型、列舉、委託、屬性等。
- 使用 camelCase（小駝峰式）來命名局部變數、參數、私有欄位。
- 介面必須以 `I` 開頭並使用 PascalCase。
- 泛型類型參數必須以 `T` 開頭並使用 PascalCase。


### 6.2 .NET 設計指南命名規則

- 公開、保護、受保護內部常數欄位必須使用 PascalCase。
- 公開、保護、受保護內部靜態只讀欄位必須使用 PascalCase。
- 不允許有公開、保護、受保護內部的非靜態欄位。

### 6.3 StyleCop 命名規則

- 所有常數欄位必須使用 PascalCase。
- 靜態只讀欄位必須使用 PascalCase。
- 非私有欄位不允許存在。
- 私有欄位必須使用 `_camelCase`（下劃線小駝峰式）。
- 局部變數必須使用 camelCase。

### 6.4 命名慣例

- 型別和命名空間 (Type and Namespace) 應使用 PascalCase (例如 MyClass, MyNamespace)。
- 介面 (Interface) 應使用 IPascalCase (例如 IMyInterface)。
- 型別參數 (Type Parameter) 應使用 TPascalCase (例如 TMyType)。
- 方法 (Method) 應使用 PascalCase (例如 MyMethod())。
- 屬性 (Property) 應使用 PascalCase (例如 MyProperty)。
- 事件 (Event) 應使用 PascalCase (例如 MyEvent)。
- 本地變數 (Local Variable) 應使用 camelCase (例如 myVariable)。
- 本地常數 (Local Constant) 應使用 camelCase (例如 myConstant)。
- 參數 (Parameter) 應使用 camelCase (例如 myParameter)。
- 公開欄位 (Public Field) 應使用 PascalCase (例如 MyField)。
- 私有欄位 (Private Field) 應使用 _camelCase (例如 _myField)。
- 公開常數欄位 (Public Constant Field) 應使用 PascalCase (例如 MyConstant)。
- 私有常數欄位 (Private Constant Field) 應使用 PascalCase (例如 MyPrivateConstant)。
- 公開靜態 readonly 欄位 (Public Static readonly Field) 應使用 PascalCase (例如 MyStaticReadonlyField)。
- 私有靜態 readonly 欄位 (Private Static readonly Field) 應使用 PascalCase (例如 MyPrivateStaticReadonlyField)。
- 列舉 (Enum) 應使用 PascalCase (例如 MyEnum)。
- 局部函式 (Local Function) 應使用 PascalCase (例如 MyLocalFunction())。
- 非欄位成員 (Non-Field Member) 應使用 PascalCase (例如 MyMember)。

## 7. 其他命名規則

- 所有命名空間、類型、委託、事件、方法、屬性等必須使用 PascalCase。
- 介面應以 `I` 為前綴並使用 PascalCase。
- 泛型類型參數應以 `T` 為前綴並使用 PascalCase。
- 函數參數必須使用 camelCase。
