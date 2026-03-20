
<h1 align="center">sakamsg</h1>

<p align="center"><i>A CLI tool for 坂道 |  齋藤飛鳥 | 山下美月 | 白石麻衣 メッセージ and 坂道 ブログ</i></p>

<div align="center">
    <a href="#">
    <img src="https://img.shields.io/badge/license-EULA-yellow" alt="License">
  </a>
  </div>

</div>

>[!NOTE]
> This is not an open source project, and I make this because I am interested on it.

>[!NOTE]
>For Yodel メッセージ.
><br>Please Try [Yodmsg](https://github.com/limangox/yodmsg) .

## Features
- Retry the download when a download error is encountered.
- Check for any missing files.

- ✅ 乃木坂46 メッセージ
- ✅ 日向坂46 メッセージ
- ✅ 櫻坂46 メッセージ
- ✅ 齋藤飛鳥 メッセージ
- ✅ 山下美月 メッセージ
- ✅ 白石麻衣 メッセージ
- ✅ 乃木坂46 BLOG
- ✅ 日向坂46 BLOG
- ✅ 櫻坂46 BLOG
- [ ] 欅坂46 BLOG
- ✅ Local blog viewer
- [ ] Local message viewer

# Recommended terminal tool (os:win)
> Use the recommended terminal tools to better support the color display of scripts
- Windows Terminal
  - [Mircosoft Store](https://apps.microsoft.com/detail/9n0dx20hk701)
  - [github](https://github.com/microsoft/terminal)
- Cmder : [Homepage](https://cmder.app/)


> [!NOTE]
> # About `refresh_token`
> * You can use [Proxypin](https://github.com/wanghongenpin/proxypin) to get your ` refresh_token `.


# How to use
### Command for Save message

>  user needs to get the `refresh token` by own.
<details>
  
  - `-r` refresh token | The `-r` command defaults saving files from 乃木坂 message app.
    
    ```
    sakamsg -r refresh_token 
    ```
  - `-hn` saving files from 日向坂 message app.
    
    ```
    sakamsg -r refresh_token -hn
    ```
  - `-s` saving files from 櫻坂 message app.
    
    ```
    sakamsg -r refresh_token -s
    ```
  - `-a` saving files from 齋藤飛鳥 message app.
    
    ```
    sakamsg -r refresh_token -a
    ```

  - `-y` saving files from 山下美月 message app.
    
    ```
    sakamsg -r refresh_token -y
    ```
  - `-mai` saving files from 白石麻衣 message app.
    
    ```
    sakamsg -r refresh_token -mai
    ```
## Saving specify member's message
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
## Download the Thumbnails、voice calling images、offical photos of all members.
  - Use `-p` to download the Thumbnails、voice calling images、offical photos of all members.
    
    ```
    sakamsg -r refresh_token -p
    ```
    > also can with `-hn / -s / -a / -y / -mai ` to save the thumbnails、voice calling images、offical photos from specify group/person.
  
    ```
    sakamsg -r refresh_token -p -hn
    ```

## Query the subscription members
  - Use `-q` Query the subscription members (Contains current members that have been subscribed to)
    ```
    sakamsg -r refresh_token -q
    ```
    > with `-hn / -s / -a / -y / -mai ` command
  
    ```
    sakamsg -r refresh_token -q -hn
    ```
</details>

## Command for Saving blog
> Special `-m` for Nogizaka46 blog group name : `3期生` | `4期生` | `新4期生` | `5期生`
> 
> Special `-m` for Hinatazaka46 blog group name : `ポカ`
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
  - use `-blog` and `-s` and `-m` to save sakurazaka member blog
    ```
    sakamsg -blog -m 守屋麗奈 -m 石森璃花 -m 山下瞳月 -s
    ```
  - use `-sc` to skipping blog integrity checking
    
    > When this feature is activated, only new blog content will be saved, and no integrity check will be performed on blogs that have already been saved locally.
    > And if you add a member who has never saved a blog before, adding the -sc command will not affect this member's blog-saving function; it will ignore the `-sc` command and fully save this member's blog.
    ```
    sakamsg -blog -sc -m 遠藤さくら
    ```
  #### Screenshot for html file
  ![ayablog](/img/blog_aya.jpg)
</details>

# Change Log
<details>

## V1.5.0
### What's New?
- Add support for ` 白石麻衣メッセージ `
- Add support for download past messages

## V1.4.1

### Change log

* Update all api.
* Fix an issue that can't save all messages from `齋藤飛鳥メッセージ`.
* Fix an issue when saving ` phoneimage / officalimage ` from `齋藤飛鳥メッセージ` and ` 山下美月メッセージ `.

## V1.4.0
### What's new
- Add support for ` 櫻坂46 ` BLOG

### Fix and Change log
- Fixed a 'request failed' issue after saving ` 齋藤飛鳥 メッセージ `
- Optimize the style of  BLOG reader
- Update the API parameters of `坂道 メッセージ `
- Fix some issue when saving ` thumbnails/photo image/official photos ` 
  - In ` MSG/image/<日向坂46> or <櫻坂46> ` folder,if the number of folders such as ` 121_藤嶌果歩 `,its pre-number is larger than 90 and also have a folder name as ` 74_藤嶌果歩 `.You can use  [merge_dir.exe](https://github.com/limangox/sakamsg/releases/download/V1.4.0/merge_dir.exe)   merge folders to correct pre-number.



## V1.3.1
### Fix and Change log
- Optimize the BLOG reader style.
- Change the save policy for message `thumbnails/photo image/official photos`. The new one will be saved to the`<group>/memberid_membername` folder.
     - <mark>If you saved a file in version 1.3.0 or earlier, download [move_sakaimg.exe](https://github.com/limangox/sakamsg/releases/download/V1.3.1/move_sakaimg.exe) to the directory `MSG/Image/group`, then double-click to run. The program will automatically migrate the files in the folder according to `memberid_membername` folder. You will have to delete the`official_photo`、`phone_images`、`thumbnail` folder from the original directory by yourself.<mark>
- Optimize the sakurasaka46 `thumbnails/photo image/official photos` save strategy, with the correct `memberid` to create the folder and save the file.



## V1.3.0
### What's new
- Add support for `山下美月メッセージ`

### Fix and Change log
- Save Blog function optimization

## V1.2.4
### What's new
- Add a group blog reader, located in `BLOG/<乃木坂46 | 日向坂46>` directory. You can use `-sc` and one group member name command to create a group blog reader quickly .eg: `sakamsg -sc -blog -m 遠藤さくら` or `sakamsg -sc -hn -m 小坂菜緒` .

### Fix and Change log
- Fix a full-width digit issue with 乃木坂46 `３期生` and `４期生` blog folder.If you already saved blogs of these groups , manually change the number to half-width digit like  `3期生` and `4期生` .
- Optimize the BLOG reader style.
- Fix a partial error in saving the HTML file for a member's blog.

## V1.2.3
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

</details>

## Support me
<div align="center">
  <a href="https://www.buymeacoffee.com/limangox"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-9e3eb2?style=for-the-badge&logo=buy-me-a-coffee&logoColor=fff" alt="BuyMeACoffe"></a>
  <a href="https://afdian.com/a/limangox"><img src="https://img.shields.io/badge/🐳爱发电-Support Me-9e3eb2?style=for-the-badge&logoColor=fff" alt="BuyMeACola"></a>
