
A CLI tool for 乃木坂46メッセージ | 齋藤飛鳥メッセージ app

![License](https://img.shields.io/badge/license-MIT-yellow)
![Language](https://img.shields.io/badge/language-python-brightgreen)

## Features
- Retry the download when a download error is encountered.
- Check for any missing files.
- Friendly error alert mechanism.

## Command
- -r refresh token 
  ```
  nogimsg -r refresh_token 
  ```
- -a Download files from saitou asuka message app.
  ```
  nogimsg -r refresh_token -a
  ```
- -m member name in Japanese.
  > You can specify multiple members with'-m'
  ```
  nogimsg -r refresh_token -m 遠藤さくら　-m 井上和 
  ```
- -p Download the Thumbnails、voice calling images、offical photos of all members.
  ```
  nogimsg -r refresh_token -p
  ```
- -q Query the subscription members (Contains current members that have been subscribed to)
  ```
  nogimsg -r refresh_token -q
  ```

