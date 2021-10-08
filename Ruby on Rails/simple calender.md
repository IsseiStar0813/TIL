datetime 属性を持つ start_time　カラムを持つモデルを用意

month_calender メソッド　月間カレンダーを作成(week_calenderにすると、週間カレンダー)
```
<%= month_calendar do |date| %>
  <%= date %>
<% end %>
```

第二引数を渡して、日付け以外の要素を表示することもできる

```
<%= month_calender  do |date,event|
   <%= date %>
    
   <%= event.title %>

表示日数をカスタム
```
<%= calendar(number_of_days: 4) do |date| %>
  <%= date %>
<% end %>
```

見た目を編集 

rails g simple_calendar:views で viewファイルが作成される
