## Gitbook使用手冊

### 重要觀念
將專案git push 至github上，使gitbook與之連接，才可在github更新的同時，gitbook內容同步更新

### 常用指令
```bash
$ gitbook init # 初始化gitbook專案

$ gitbook serve # 本地端模擬上傳至gitbook時的頁面

$ gitbook install # 依book.json安裝其使用之套件
```

### 重要文件
* SUMMARY.md
    - 整本gitbook的目錄
* README.md
    - 整本gitbook的大綱
* book.json
    - 配置、套件羅列
    - 其套件安裝後，需編寫設定，才會生效

### Plugins
- 於plugin名稱前加上減字號，代表省略其套件
- `gitbook install`指令會把整個專案的套件列表全下載，若想要省時間，可使用`npm install gitbook-plugin-套件名`安裝單一套件
- 推薦Plugins
    - github
        ```json
            "github": {
                "url": "https://github.com/hanc1027/Telegram_Intro"
            }
        ```
    - github-buttons
        ```json
            "github-buttons": {
                "repo": "hanc1027/Telegram_Intro",
                "types": [
                    "star"
                ],
                "size": "small"
            }
        ```
    - pageview-count
    - edit-link
        ```json
            "edit-link": {
                "base": "https://github.com/hanc1027/Telegram_Intro/edit/master",
                "label": "編輯本頁"
            } 
    ```