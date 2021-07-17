config/environments/development.rbに下記を記載し、ホワイトリストに許可したいhostを追加する。
```
Rails.application.configure do
（中略）
  config.hosts << "<許可したいホスト名>"
（中略）
end
```
