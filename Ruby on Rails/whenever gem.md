処理を定期的に自動で実行させる

wheneveriseとコマンドを打ち、作成された、config/schedule.rbに処理を記述

ジョブの作成

```
# Example:
  #
  # set :output,  "/path/to/my/cron_log.log"    ...(1)
  #
  # every 2.hours do                            ...(2)
  #   command  "/usr/bin/some_great_command"
  #   runner "MyModel.some_method"
  #   rake "some:great:rake:task"
  # end
  #
  # every 4.days do                             ...(3)
  #   runner  "AnotherModel.prune_old_records"
  # end
```

1 set :outputにログファイルの出力先を指定　

2,3 ジョブ（処理）を実行するタイミングの指定　2は2時間ごと　3は4日ごと　3のような、days指定の場合、atで実行する時間を指定できる

ジョブの内容をブロック内に記述

『command』
　　sh 等のOS上のコマンドを実行したい場合に利用
　　引数にコマンドを渡す
『runner』
　　モデルに定義されたメソッドを呼び出したい場合に使用　 
　　引数には「モデル名」と「メソッド名」をドットで連結した文字列を渡す
『rake』
　　rakeコマンドを指定


