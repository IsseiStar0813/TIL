datetime 属性を持つ start_time　カラムを持つモデルを用意

month_calender メソッド　月間カレンダーを作成(week_calenderにすると、週間カレンダー)
```
<%= month_calendar do |date| %>
  <%= date %>
<% end %>
```

表示日数をカスタム
```
<%= calendar(number_of_days: 4) do |date| %>
  <%= date %>
<% end %>
```
