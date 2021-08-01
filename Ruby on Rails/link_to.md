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
