flash[:<キー>] = <メッセージ>で登録し、flash.each do |message_type, message|で出力

flash→次のアクションまでデータを保持する→redirect_toと一緒に使う
flash.now→次のアクションに移行した時点でデータが消える→renderと一緒に使う
