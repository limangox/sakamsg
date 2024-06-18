
A CLI tool for (乃木坂 | 日向坂 | 櫻坂 | 齋藤飛鳥) メッセージ app and 坂道 Blog

![License](https://img.shields.io/badge/license-MIT-yellow)

## Support me
<div align="center">
  <a href="https://www.buymeacoffee.com/limangox"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-9e3eb2?style=for-the-badge&logo=buy-me-a-coffee&logoColor=fff" alt="BuyMeACoffe"></a>
  <a href="https://afdian.net/a/limangox"><img src="https://img.shields.io/badge/🐳爱发电-Support Me-9e3eb2?style=for-the-badge&logoColor=fff" alt="BuyMeACola"></a>

</div>

## Features
- Retry the download when a download error is encountered.
- Check for any missing files.
- Friendly error alert mechanism.

- ✅ 乃木坂46 メッセージ
- ✅ 日向坂46 メッセージ
- ✅ 櫻坂46 メッセージ
- ✅ 齋藤飛鳥 メッセージ
- ✅ 乃木坂46 BLOG
- ✅ 日向坂46 BLOG
- [ ] 櫻坂46 BLOG

# Notice
- In Mac OS, use `./sakamsg` command to ensure that the running path is accurate, otherwise there will be a `command sakamsg not found ` error.

# Recommended terminal tool (os:win)
> Use the recommended terminal tools to better support the color display of scripts
- Windows Terminal
  - [Mircosoft Store](https://apps.microsoft.com/detail/9n0dx20hk701)
  - [github](https://github.com/microsoft/terminal)
- Cmder : [Homepage](https://cmder.app/)
# How to use
### Command for Save message

>  user needs to get the `refresh token` by own
<details>
  
  - `-r` refresh token | The `-r` command defaults saving files from nogizaka message app.
    
    ```
    sakamsg -r refresh_token 
    ```
  - `-hn` saving files from hinatazaka message app.
    
    ```
    sakamsg -r refresh_token -hn
    ```
  - `-s` saving files from sakurazaka message app.
    
    ```
    sakamsg -r refresh_token -s
    ```
  - `-a` saving files from saitou asuka message app.
    
    ```
    sakamsg -r refresh_token -a
    ```
  - `-m` member name in Japanese.
    
    > You can specify multiple members with'-m'
    
    ```
    sakamsg -r refresh_token -m 遠藤さくら　-m 井上和 
    ```
    > When the `-hn` command is added, the specified hinatazaka member message file will be downloaded
  
    ```
    sakamsg -r refresh_token -hn -m 小坂菜緒　-m 金村美玖 
    ```
    
    > When the `-s` command is added, the specified sakurazaka member message file will be downloaded
    ```
    sakamsg -r refresh_token -s -m 守屋麗奈 -m 森田ひかる
    ```
  - `-p` Download the Thumbnails、voice calling images、offical photos of all members.
    
    ```
    sakamsg -r refresh_token -p
    ```
    > also can with `-hn` to save the thumbnails、voice calling images、offical photos of all members from hinatazaka.
  
    ```
    sakamsg -r refresh_token -p -hn
    ```
    > also can with `-s` to save the thumbnails、voice calling images、offical photos of all members from sakurazaka.
  
    ```
    sakamsg -r refresh_token -p -s
    ```
  - `-q` Query the subscription members (Contains current members that have been subscribed to)
    ```
    sakamsg -r refresh_token -q
    ```
    > with `-hn` command
  
    ```
    sakamsg -r refresh_token -q -hn
    ```
</details>

### Command for Save blog
> Special `-m` for Nogizaka46 blog group name : `3期生` | `4期生` | `新4期生` | `5期生`
> 
> Special `-m` for Nogizaka46 blog group name : `ポカ`
> 
> use `-blog` and `-m` to save nogizaka member blog
<details>

  - add the member's Japanese name after `-m`
    ```
    sakamsg -blog -m 遠藤さくら -m 岩本蓮加 -m 3期生 -m 井上和
    ```
  - use `-blog` and `-hn` and `-m` to save hinatazaka member blog
    ```
    sakamsg -blog -m 加藤史帆 -m 小坂菜緒 -m 上村ひなの -hn
    ```
  - use `-sc` to skipping blog integrity checking
    
    > When this feature is activated, only new blog content will be saved, and no integrity check will be performed on blogs that have already been saved locally.
    ```
    sakamsg -blog -sc -m 遠藤さくら
    ```
  #### Screenshot for html file
  ![ayablog](/img/blog_aya.jpg)
</details>


# Change Log
##V1.2.3
### Fix
- Fixed an incorrect image extension when saving a blog image.

## V1.2.2
### What's New
- Added New version detection function.
- Add the function of skipping blog integrity checking. If you only want to save the new blog, please use `-sc` command to skip the old blog integrity checking.

### Fix
- Optimise the logic of getting the list of Hinagizaka's blogs.
- Change the content path of saving html to relative path. If you have already saved the blog (without deleting the saved blog), please get it again, the file path in html will be updated to relative path.
- Fixed the problem that some blog image url paths were encoded with url code, which caused errors in saving and displaying.
- Now the blog list of different groups use the colour of the corresponding group,the saved html file will be updated when you save the blog next time.

## V1.2.1
- Optimize the save policy and retry mechanism for saving blog
- Fixed the issue where generating HTML files failed when saving some members' blogs.

## V1.2.0
- Support Hinatazaka46 Blog.
- Fix some issues when saving blog html.
- Optimize the structure of the generated HTML files.

## V1.1.1
- Fix issue when update blog html

## V1.1.0
- Add Nogizaka Blog Support.Please use `-blog` and `-m ` without `-r` to download blog.
- A simple local blog reader will be generate when save blogs.


