---
title: テストページ
---

このページは、GitHub Desktopで作成したページが、別のdomainへ転送出来るのかを試すために作ったものです。<br>
処理としては、CNAMEを書いたのみで、残りは、GitHub pagesのもともとの機能を使用しています。<br>
[基本的にはこちら](https://docs.github.com/ja/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#%E3%82%B5%E3%83%96%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E3%82%92%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B)を参照しています。<br>

## このページの構成
もともと、このページは、[https://ShohTagawa.github.io](https://ShohTagawa.github.io)をgithubで持っています。<br>
個人所有しているdomainである、geophysica.orgのDNSの設定をいじり、CNAME設定を変えています(下記に写真が表示されます)。<br>
  ![](support/DNS.PNG)  
※ サーバーは、xserverの管理です<br>
上記の処理を行って、数時間待った後(DNSの順次更新)、GitHub側のSettingsにある、pages設定のCustum domainを登録します。<br>
その結果、カスタムdomainである、[http://geophysica.org/](http://geophysica.org/)で表示されるように致しました。<br>

## リンクのテスト
アドレスを転送する上で、もっともネックになるのは、様々な階層の既存ページへのアドレスに対するリンクやブックマークが動かなくなることです。<br>
ここでは、その点について、テストします。<br>

下記は、リンクが動くかのテストです。下記のリンクタイプが想定され、それぞれ作ってみました。<br>
[リンク①](what_not_new)：おなじ階層の相対リンク。旧直リンクは、[https://ShohTagawa.github.io/what_not_new](https://ShohTagawa.github.io/what_not_new)<br>
[リンク②](support/)：一つ下の階層への相対リンク(index.md)。旧直リンクは、[https://ShohTagawa.github.io/support/](https://ShohTagawa.github.io/support/)<br>
[リンク③](support/howto)：一つ下の階層への相対リンク(howto.md)。旧直リンクは、[https://ShohTagawa.github.io/support/howto](https://ShohTagawa.github.io/support/howto)<br>
[リンク④](support/test.jpg)：一つ下の階層の画像ファイル。旧直リンクは、[https://ShohTagawa.github.io/support/test.jpg](https://ShohTagawa.github.io/support/test.jpg)<br>
[リンク⑤](support/howto#1前提)：一つ下の階層の相対リンク(howto.md)中のタグ1へのリンク。旧直リンクは、[https://ShohTagawa.github.io/support/howto#1前提](https://ShohTagawa.github.io/support/howto#1前提)<br>

## 気になる点
- 英語ページへのリンクなどはきちんと動くか?
- Googleのクロールは、どちらのサイトで登録されるか。
- httpsの問題はないか。

## 設定手順
- 設定した手順については、howtoにのせました。