処理を定期的に自動で実行させる

config/schedule.rbに処理を記述

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


