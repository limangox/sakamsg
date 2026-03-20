
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

## Saving letters with `-l`

> - `sakamsg -r refresh_token -l` to save all letters
> - `sakamsg -r refresh_token -m 遠藤さくら -l` to save letters sent to 遠藤さくら
> - `sakamsg -r refresh_token -m 大野愛実 -hn -l` to save letters sent to 大野愛実

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


## Support me
<div align="center">
  <a href="https://www.buymeacoffee.com/limangox"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-9e3eb2?style=for-the-badge&logo=buy-me-a-coffee&logoColor=fff" alt="BuyMeACoffe"></a>
  <a href="https://afdian.com/a/limangox"><img src="https://img.shields.io/badge/🐳爱发电-Support Me-9e3eb2?style=for-the-badge&logoColor=fff" alt="BuyMeACola"></a>
