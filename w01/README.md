# 來個Hello World

## 步驟
1. 初始化專案資料夾 -> package.json
2. 為專案安裝 webpack -> node_modules, package-lock.json
3. 設置 package.json, 用來執行webpack打包程式碼
4. 創建目錄 -> src(專案原始碼), dist(經webpack編譯打包後的瀏覽器可執行檔案)
5. 利用webpack打包編譯index.js


## 實作
- 初始化
```bash
npm init
```
- 安裝 webpack
```bash
npm install webpack webpack-cli --save-dev
```
- 創建目錄代碼目錄
```bash
mkdir src dist
```
- 利用 webpack build
```bash
npm run build
```
