# webpack

1. 開發環境建置
### 先來安裝個 nvm 吧！
    - nvm( Node Version Manager ) : 管理 nodejs 版本的工具
    - 安裝 : curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
    - zsh: command not found: nvm解決 :
    ```bash
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
    ```
    - nvm 指令 :
        - nvm -v : 確認nvm版本
        - nvm ls : 已安裝的 nodejs 版本
        - nvm ls-remote : 可安裝的 nodejs 版本
        - nvm install 版本號 : 下載指定的nodejs版本號
        - nvm use 版本號 : 使用指定的nodejs版本號
    - node 指令（nvm use 後可使用） :
        - node -v : nodejs版本確定
    - npm（ Node Package Manager ） 指令（nvm use 後可使用）:
        - npm - v : Node Package Manager版本確定

2. webpack 的核心概念： "注入( entry )"

3. 利用 webpack 建置前端專案 :
    - 建立專案目錄：
    ```bash
    mkdir w00
    ```
    - 使用 npm 初始化專案 :
    ```bash
    npm init
    ```
    - 使用 npm 在專案中安裝 webpack webpack-cli
    ```bash
    npm install webpack webpack-cli --save-dev
    ```
    - 新增並編寫 webpack 打包規則設定檔：
    ```bash
    touch webpack.config.js
    ```
    ```vim
    module.export = {
        entry: './src/index.js', # 欲打包文件的進入點（路徑）
        output: {
            filename: 'index-bundle.js', # 打包編譯後檔案的輸出名
        }
    }
    ```
    - 編寫打包 ( webpack ) 時使用的腳本 ( script ):
    ```bash
    vim package.json
    ```
    ```vim
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "start": "webpack" # 新增自定義 webpack 打包編譯指令為 -> start
    },
    ```
    - 新增未打包源代碼目錄：
    ```bash
    mkdir src
    touch src/index.js
    ```
    - 利用 webpack 對 ./src/index.js 打包編譯：
    ```bash
    npm run build
    ```

4. 利用 npm 安裝簡易的 web 服務器 http-server：
    - 安裝：
    ```bash
    npm install http-server
    ```
    - 從當前路徑在3000端口上啟動服務器
    ```bash
    npx http-server ./dist/main.js -d -c -a -p 3000
    ```
    - http-server版本確定：
    ```bash
    npx http-server -v
    ```