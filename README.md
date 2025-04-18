# hkimjp/todo

## Todo

* LXD クライアントの使用可能メモリを増やす
* NextCloud: shared フォルダの使い方。
* postfix, dovecot のコンフィグをコピーするか。これが最も問題少ないか。
* rainloop は apache->nginx のため、ひと踏ん張り必要。
* 踏み台 ssh が 1/2 の割合で失敗する理由。VPN もしばし途中で切れちゃうぞ。大学ネットが怪しい。
  rsa キーを有効にするとこの現象は消える。なぜ？
* dhcp15 を固定 IP に。
* dhcp29 の IP を固定する。cony の代わりだから 150.69.84.221.
* raspberry (bind) を収容する。あるいは逆に DHCP と LDAP を吐き出す。
* iPhone からの ICMP too large
* 全てを　workspace/ 以下にまとめて、clojure, teaching, projects, etc. は
  そこへのシンボリックリンクにしたらどうか？

## 2025-04-14-SNAPSHOT

* restore container postgres databases
  see ~/docker/postgresql@17


## 2025-04-13

* dump postgresql container

* L22: 後期の授業、再履修、ギブアップもあるだろう。科目名を分けた。
  後期の python は python-b になる。

    update users set subj='python-a'

* L22 の pg16 でダンプしたプレーンテキストは m64 の pg17 でリストアできた。
* typing-ex: スコアをリセット
* py99: 2024: 回答をリセット。投稿とコメント、ストックのテスト。

## 2025-04-08

* typing-ex 4.31.0. 一旦バージョン番号に v をつけたら、それを続けないとどれが新しいか分かりにくくなるか。
* cntl のメールトラブル - ブラックリスト入りの sender をそのまま .forward に乗せて来て、
  ブラックリストにはない cntl のメールサーバが mns の fail2ban に捕まった？
* fail2ban script - fail2ban-client banned, faileban-client unban ip ... があり、
  それでじゅうぶん対応できそう。そんなコマンド、あった？
* ip.melt - ぞのさんの調査を反映させた。IA, IB のレンジ。
* github.com/hkim0331/<project>/.git/config 中の github.com を github-hkim0331 に書き換える。

```
for i in $(ls */.git/config); do
  grep github.com $i ; sed -i 's/github.com/github-hkim0331/' $i
done
```

* stopped/disabled isc-dhcp-server6

```
root@hp# systemctl stop isc-dhcp-server6.service
root@hp# systemctl disable isc-dhcp-server6.service

```

## 2025-04-07

* dhcp15 ufw.
* apt install postfix dovecot-imapd dovecot-pop3d
* 授業準備 -  projects/l22/.git/config を書き換えた。
* updated request-map(ip) - added KIT-IA and KIT-IB.
* 授業準備 - L22.

## 2025-04-06

* raspberry ufw ok.
* sweep を rabbit にインストール。
* dhcp15.mns:/usr/local/bin/remove-unused-bridges.sh
* dhcp15.mns: start dhcp server
* copy cony.mns:/var/lib/dhcp to dhcp15.mns:/var/lib/dhcp
* copy cony.mns:/etc/dhcp to dhcp15.mns:/etc/dhcp
* cony.mns: stop dhcp server
* RSA 鍵と ED25519 鍵の両方がある PC から ssh-copy-id すると ED25519 鍵がコピーされるが、
  ssh の認証は RSA 鍵でおこなわれる。何かオプションがありそう。
* komura さんのアカウントを新サーバーにコピー。ldif で。

```
    # systemctl stop slapd
    # slapadd -l komura.ldif
    # systemctl start slapd
    $ id komura
    uid=10043(komura) gid=10001(users) groups=10001(users)
```

* base64 デコード。Mac から出したメールをデコード専用スクリプトを作る。
  => ヘッダを外し /opt/homebrew/opt/coreutils/libexec/gnubin/base64　でよい。
  ~/bin/base64 は改行の扱いができてない。

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
