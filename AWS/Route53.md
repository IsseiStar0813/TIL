# Route53とは
AWSが提供する権威DNSサービス

ネームサーバの役割を果たす

## ホストゾーン　
DNSのリソースレコードの集合体　ゾーンファイルのようなもの

## レコードセット
リソースレコードのこと

- NS そのドメインを管理するネームサーバとの紐付け
- SOA　そのドメインのゾーンの管理情報
- A　ドメイン名と、IPアドレスの紐付け

## ルーティングポリシー
レコードセットに対してどのようなルーティンを行うかを決める

## ヘルスチェック
サーバーの稼働状況をチェック

- シンプルルーティング　
一般的なDNS　1つのレコードに対して、1つのIPアドレスが存在する

- 加重ルーティング

0～255 の値によって、問い合わせの方向を変化させる
40%のルーティングを1.1.1.1に流す、60%のルーティングを2.2.2.2に流すというようなことが出来る。
ABテストの検証などで使用されることがある

- 位置情報ルーティング

位置情報によって、優先度が変わる
地域別によって、配信する情報を変化させたいときに利用する

- レイテンシールーティング

レイテンシーが最小になるリソースを優先的にアクセスさせるルーティング方式
世界中にシステムを展開した際に、近いリソースにアクセスをさせたほうが早く回答が出来る。

- フェイルオーバールーティング

プライマリとセカンダリで分けて
プライマリのヘルスチェックに失敗したらセカンダリにアクセスがされるようになる。

# route53を使い、ドメインでwebサイトにアクセスできるようにする
1. ドメインを取得
2. ネームサーバーを、Route53へ変更(必要な場合)
3. ドメイン名とIPアドレスをAレコードで紐付け

