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
    