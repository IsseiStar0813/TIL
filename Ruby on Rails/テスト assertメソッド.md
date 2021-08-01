* assert 式がtrueの場合に、テストが成功となる
* assert_not 式がfalse の場合に、テストが成功となる
* assert_select 特定のhtmlタグが存在する場合に成功　countでいくつ存在するかを指定できる　リンクの場合は、"a[href=?]",パス　のように書く
* assert_difference 式の実行前後で、第1引数に渡した値の数が、第2引数に渡した数値分変化した場合成功
```
assert_difference 'User.count', -1 do
  delete user_path(@non_admin)
end
```
* assert_no_difference 式の実行前後で、引数に渡した値の数が変化しない場合に成功
* assert_redirected_to 渡したリダイレクト先にリダイレクトされたら成功
* assert_match 第一引数の正規表現の値と第二引数の値がマッチすれば成功になる
* ```
#基本構文
assert_match(正規表現, 文字列 [, メッセージ])

#HTMLを評価するときの使い方(Railsチュートリアル第13章より)
assert_match @user.microposts.count.to_s, response.body
```
