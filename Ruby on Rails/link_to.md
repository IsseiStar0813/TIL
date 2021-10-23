show, update, destroyアクションの場合はオブジェクト名だけで指定できる

```
<% @microposts.each do |micropost %>|
 <%= link_to "delete", micropost_path(micropost), method: :delete %>
・
・
```
同義
```
<% @microposts.each do |micropost %>|
<%= link_to "delete",micropost,method: :delete %>
・
・
```

文字列以外のタグなど（以下の例ではボタン)にリンクを付与したい場合 

```
<%= link_to user_path do %>
  <button>ボタン<\button>
<% end %>
