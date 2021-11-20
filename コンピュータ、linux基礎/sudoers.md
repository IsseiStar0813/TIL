# sudoers 
どのユーザーが何を実行できるかを記述した設定ファイル /etc/sudoers に設定ファイルがある

## visudoコマンド
sudoersファイルを安全に編集するためのコマンド

複数の同時編集に対してsudoersファイルをロックし、基本的な健全性チェックを提供し、解析エラーをチェックする

基本的には安全のため、visudoで編集する方が良い

## 基本構文
誰が どのホストで = (誰として) 何を

```
rootユーザはどこでも、誰としてでも何でもできる
root ALL=(ALL:ALL) ALL

wheelグループのユーザはどこでも、誰としてでもパスワード無しで何でもできる
%wheel ALL=(ALL:ALL) NOPASSWD: ALL

bobはaliceとして閲覧コマンドを実行できる
bob ALL=(alice) /bin/ls, /bin/cat
```
