# hkimjp/todo

## Todo

* fail2ban-client-status-all
* fail2ban-unbanip xxx.yyy.zzz.www
* LXD クライアントの使用可能メモリを増やす
* NextCloud: shared フォルダはどう使う？
* sweep と同等品を mns サーバーに。
* DHCP isc-dhcp-server
* rainloop (eq でトライした)
* postfix
* dovecot
* base64 デコード。Mac から出したメールをデコード専用スクリプトを作る。
* (refer-clojure :exclude [read-string]) はどこへ書く？
* komura さんの LDAP データのコピー。LDIF で？

## 2025-04-05

* ip.melt に favicon.ico
* babashka で telemere のライブラリエラー。大人しく timbre すれば問題ない。
* rsync-homes.bb - 2 度目は 3 分で完了した。

    /dev/nvme0n1p2  468G   86G  358G  20% /


### rabbit:/home/* の転送練習。

* rsync-homes.bb - 予想では実行に 1h。-> 1h35mn.


## 2025-04-04

* request-map 0.7.0 - アクセスログをとる。IPから推測されるロケーションを表示する。
* **todo** KIT-IA, KIT-IB の表示。

## 2025-04-03

* `mkdir mails && mv resources/* mails/`
* copy `.gitignore` from neil's app.
* make the repository public again.
* request-map 0.6.0. 短期 DHCP ゾーンにいたら知らせられるように。動作チェック未実施。
* request-map 0.6.1. バグフィックス。動作チェック。
* request-map 0.6.2.
* C216 のルータを 150.69.84.216 に誘導。
* rsync-home.bb は rabbit から、1GB/min 程度。
* request-map 0.6.3: login by default middleware.
* request-map 0.6.4: a bug in 0.6.3.

## 2025-04-02

* initialized repository.
* created komura's account.
* nsakai can not forward mails from 'cntl.kyutech' to 'hamilton'?
* TODO アプリの作成 - github の利用でお茶をにごす。

### NextCloud (nc.melt)

* email 設定
* nc.melt で mns メールを読む。
* 「"opcache.memory_consumption" を "128" よりも高い値で適用することをおすすめします」 の表示が消えた。何もしてないぞ？
* パスキーでログイン

## 2025-04-01

* rabbit: サーバアカウント、メールリストの整理
* 鎌田さん: メールの転送
* 田中さん: アーカイブを POP3 でダウンロードできるか？
* 紅村さん: 新アカウント作成、LAM の準備がまだだったので、math@mns メールリストに慶応のアドレスを追加。

## License

Copyright © 2025 Hkim

Distributed under the Eclipse Public License version 1.0.
