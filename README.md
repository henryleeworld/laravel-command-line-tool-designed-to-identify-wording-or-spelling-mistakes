# Laravel 12 用於識別措辭或拼字錯誤的命令列工具

引入 peckphp 的 peck 套件來擴增用於識別措辭或拼字錯誤的命令列工具，可以自然地融入您的工作流程，利用 GNU 的開源拼字檢查程式 Aspell 的強大功能檢查您的程式碼基底每個角落。

## 使用方式
- 該套件繪圖需要安裝 Aspell 工具。
> 如果是在電腦作業系統 Debian 或 Ubuntu，可以執行指令來安裝：sudo apt-get install aspell {語言字典，例如：aspell-en}。
> 如果是在電腦作業系統 MacOS，可以使用 Homebrew 來安裝：brew install aspell。
> 如果是在電腦作業系統 Windows，可以參考官方教學[連結](https://scoop.sh/)進行一步步安裝。
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 你可以使用 `./vendor/bin/peck` 指令來執行措辭或拼字錯誤檢查。
```sh
$ ./vendor/bin/peck
```

----

## 畫面截圖
![](https://i.imgur.com/Rs928uU.png)
> 檢查措辭或拼字錯誤
