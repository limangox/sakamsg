
A CLI tool for 乃木坂46メッセージ | 日向坂46メッセージ | 櫻坂46メッセージ| 齋藤飛鳥メッセージ app

![License](https://img.shields.io/badge/license-MIT-yellow)
![Language](https://img.shields.io/badge/language-python-brightgreen)

## Features
- Retry the download when a download error is encountered.
- Check for any missing files.
- Friendly error alert mechanism.

## Command

- `-r` refresh token | The `-r` command defaults download files from nogizaka message app.
  
  ```
  sakamsg -r refresh_token 
  ```
- `-hn` Download files from hinatazaka message app.
  
  ```
  sakamsg -r refresh_token -hn
  ```
- `-s` Download files from sakurazaka message app.
  
  ```
  sakamsg -r refresh_token -s
  ```
- `-a` Download files from saitou asuka message app.
  
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
  > also can with `-hn` to Download the Thumbnails、voice calling images、offical photos of all members from hinatazaka.

  ```
  sakamsg -r refresh_token -p -hn
  ```
  > also can with `-s` to Download the Thumbnails、voice calling images、offical photos of all members from sakurazaka.

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
  > with `-s` command
  ```
  sakamsg -r refresh_token -q -s
  ```

