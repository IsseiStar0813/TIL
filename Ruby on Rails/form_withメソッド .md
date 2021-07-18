# formを作成するメソッド
* データベースに保存しない場合
```
<%= form_with url: "パス" do |form| %>
  フォーム内容
<% end %>
```
* データベースに保存する場合
```
<%= form_with model: モデルクラスのインスタンス do |form| %>
  フォーム内容
<% end %>
```
* newメソッドで作成した,空のインスタンスを渡した場合、自動的に同じコントローラのcreate アクションに送られる。
* undefinedmethod error　*** path が、ルーティングは合っているのに出た場合

原因　form_withは自動的に複数形のpathを生成するので、pathが単数形の場合エラーが起きる

対策　urlを指定する　　参考https://qiita.com/annaaida/items/ae38de82526bf5b4aa73
