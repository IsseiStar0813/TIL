# formを作成するメソッド
データベースに保存しない場合
```
<%= form_with (url: "パス" #場合によってscope,localの指定)　do |f| %>
<%= f.label :〇〇 %>
<%= f.〇〇_field :　%>
・
・
・
<%= f.submit %>
<% end %>
```

データベースに保存する場合
```
<%= form_with (model: モデルクラスのインスタンス #場合によってlocal,scopeの指定)　 do |f| )%>
<%= f.label :〇〇 %>
<%= f.〇〇_field :　%>
・
・
・
<%= f.submit %>
<% end %>
```
newメソッドで作成した,空のインスタンスを渡した場合、自動的に同じコントローラのcreate アクションに送られる。

local: trueがない場合、RailsではAjaxによる送信という意味になる。普通にHTMLとしてフォームを送信する場合にlocal: trueが必要になる

## undefinedmethod error　*** path が、ルーティングは合っているのに出た場合

原因　form_withは自動的に複数形のpathを生成するので、pathが単数形の場合エラーが起きる

対策　urlを指定する　　予めpathは複数形になるようにしておく.
参考 https://qiita.com/annaaida/items/ae38de82526bf5b4aa73

## divで囲んだとき、リロードをしないと投稿できない不具合が起こる

原因 formがdivをまたいでしまうと、turbolinksがうまく動作しなくなる

対策　一つのformごとにdivで囲み、formがdivをまたがないようにする 参考　https://qiita.com/taro03/items/4973c1c14798c1601d6e

## オプション

:placeholder =>　"値"　でplaceholder 設定
