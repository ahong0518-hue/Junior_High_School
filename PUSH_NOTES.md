# Push 慣例(給以後每次 push 用)

## 每次新增檔案都要做的事

1. **noindex 防爬蟲**:每個新的 `.html` 檔案 `<head>` 裡要加一行
   ```html
   <meta name="robots" content="noindex, nofollow">
   ```
   repo 根目錄已有 `robots.txt`(全站 Disallow),html 內的 noindex 是雙重保險,新檔案也要補上。

2. **資料夾要有 `index.html`**:每個科目/主題資料夾底下要有一個 `index.html`,列出該資料夾裡所有內容的卡片連結(照根目錄 `index.html` 的卡片式風格)。新增檔案時記得把卡片加進對應的 index.html。

3. **內容頁要能「回得去」**:每個實際內容頁(不是 index.html)頂端要有一個小型導覽列,至少包含:
   - 🏠 回首頁(連到根目錄 `index.html`,依資料夾深度調整 `../` 數量)
   - 連到所在科目/主題的 `index.html`
   - 如果同一批內容有多個檔案互相關聯(例如講義+練習題),彼此之間互相連結

   範例(地理/中國行政區背誦講義.html 用的格式):
   ```html
   <nav style="font-size:0.85rem;margin-bottom:10px">
     <a href="../index.html">🏠 回首頁</a> › <a href="index.html">🗺️ 地理</a> › 中國行政區背誦講義
     | <a href="中國行政區填空地圖_列印版.html">📝 前往填空地圖練習 →</a>
   </nav>
   ```
   如果頁面有列印功能(`@media print`),導覽列要放在 print 時會隱藏的容器裡(例如 `.toolbar`),避免印出來多一排連結。

4. **根目錄 index.html 也要更新**:新增一個新科目資料夾時,記得在根目錄 `index.html` 的 `<main>` 裡加一張卡片連過去。

## 目前的資料夾結構

- `理化/國2上/`
- `數學/`
- `地理/`

## Repo

https://github.com/ahong0518-hue/Junior_High_School
