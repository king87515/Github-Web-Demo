---
title: github 架設網頁
tags: github
categories: github
---

# test

[test](https://king87515.github.io/test/)


## Github 架設網頁
[TOC]
## Step 1 : 建立 github 帳號
這部分我我就跳過，註冊很簡單，我就附上網路的教學[開始使用 GitHub](https://progressbar.tw/posts/3)。
建立完成如下圖:
![](https://i.imgur.com/9q0IXt1.png)

## Step 2 : 創建 repository (以下我簡稱為repo)
建立完帳號，就可以創建屬於你的repository
### 點選 new repository
![](https://i.imgur.com/zVxISm9.png)
### Create repository name
* repository name 就是你的專案名稱 (這裡範例我使用 test 作為我的repo_name)
* 通常我都會把 README 初始化打開 
![](https://i.imgur.com/aQh1X3X.png)
* create repository 完成後如下
![](https://i.imgur.com/7f3cFd3.png)

* PS : 我習慣在github網頁上建repo，再把我的資料(網頁、檔案等等)在cmd用指令add/push上去，若都要從cmd那裏建立的話也是可以的唷。


## Step 3 : 把 repo 設定為 github page
* 點選 settings
![](https://i.imgur.com/40V54pt.png)

* 將框框選項改為 `master branch`
![](https://i.imgur.com/EgtOJ90.png)

* github pages的網址結構是 `http://帳號.github.io/repo_name/file_name`，沒有細分到有 file_name 就不需要，像我這個例子之後的網址就是 `https://king87515.github.io/test/`
    * 在能正確work這個網址前，要先學 git 的下載與操作

## Step 4 : git 的下載
* [git 下載教學 for windows](https://gitbook.tw/chapters/environment/install-git-in-windows.html) (MACOS預設好像就有 git，這裡我就用以 windows 為主)
* 下載完成後，使用快捷鍵 `windows+R` 進入 CMD 命令提示字元
* 檢查是否有git版本
    輸入 `git --version` 
    ![](https://i.imgur.com/fhndYvj.png)


## Step 5 : git 的操作
這裡我只提目前會用到的指令部分。

* 將建立好的 repo (你的 repo 網址)下載/複製到本地端指定目錄
```bash
git clone https://github.com/帳號/repo_name
```
![](https://i.imgur.com/5lldNnU.png)
* 我的例子 : 利用 git 將 test 放到本地端就可以進行版本控管。
* clone 完成，檔案及路徑如下
![](https://i.imgur.com/qwa4DAm.png)
* 接下來將你的專案的資料檔案放到此目錄裡面，這裡我用 `index.html` 當我的專案檔案
![](https://i.imgur.com/hhlcxHw.png)
* 你將檔案新增到本地端，但是 github 上並沒有做更動，所以這時候就要將本地端新增的檔案更新到 github 上。
* `cd repo` 進入到你的目錄
![](https://i.imgur.com/G9uui3i.png)

* 讓 github 知道你是誰
```bash 
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
![](https://i.imgur.com/d1wGuwd.png)

* 針對版本控管
```bash
git add . //將 repo_name 資料夾裡的檔案一次全部加入
git commit -m "註解內容" //對所加入檔案新增註解
git push //將上述步驟推上去 github
git pull //把檔案抓下來本地端，確保與 github 上一致，每次修改都要 push 上去 pull 下來
```
![](https://i.imgur.com/bct0BW7.png)

* 這時候重新整理你的 github 網頁，就會有新增的檔案了
![](https://i.imgur.com/8GTSG4r.png)

* 此時輸入網址 `http://帳號.github.io/repo_name/file_name`，像我這個例子之後的網址就是 `https://king87515.github.io/test/`，就完成了。
    * github 在資料夾中有多個網頁的話，預設的進入點就是叫做 `index.html` ! 所以專案的起始進入的網頁檔名就需要改成 index.html，如果只有一個 .html 那就沒差。


