---
title: テストページ
---

このページは、GitHub pagesで作成したページが、別のdomainに書き換えられるのかを試すために作ったものです。<br>
処理としては、CNAMEを書き換えただけです。残りはGitHub pagesがもともと、持っている機能を使用しています。<br>
<a href="https://docs.github.com/ja/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#%E3%82%B5%E3%83%96%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E3%82%92%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B" target="_blank">基本的にはこちら</a>を参照しています。<br>

## ページの構成
旧URL：[https://ShohTagawa.github.io/](https://ShohTagawa.github.io)<br>
  GitHub Pages管理<br>
新URL：[https://geophysica.org/](http://geophysica.org/)<br>
  個人管理のdomain (xserver社で購入・管理、DNSレコードを登録)<br>

## 何をしたか
このページはもともと、GitHub上で更新されている[https://ShohTagawa.github.io/](https://ShohTagawa.github.io/)です。<br>
個人所有しているdomainである、geophysica.orgのDNSのCNAME設定を変えて、そちらで見えるように致しました(下記に画像が表示されます)。<br>
  ![](support/dns.PNG)  
※ 個人のdomainは、xserver社で購入・管理しているものです。<br>
次に、時間待った後(DNSの順次更新)、GitHub側のSettingsにある、pages設定のCustum domainを登録しました。<br>
また、httpsをenforceする設定をonにしました。<br>
結果、カスタムdomainである、[https://geophysica.org/](http://geophysica.org/)で、[https://ShohTagawa.github.io/](https://ShohTagawa.github.io/)が表示されるようになりました。<br>

## リンクのテスト
アドレスを転送する上で、もっともネックになるのは、様々な階層のページに対する既存のリンクやブックマークが動かなくなることです。<br>
ここでは、その点について、テストします。<br>
下記は、リンクが動くかのテストです。下記のリンクタイプが想定され、それぞれ作ってみました。<br>
[リンク①](what_not_new)：おなじ階層の相対リンク。旧URLは、[https://ShohTagawa.github.io/what_not_new](https://ShohTagawa.github.io/what_not_new)<br>
[リンク②](support/)：一つ下の階層への相対リンク(index.md)。旧URLは、[https://ShohTagawa.github.io/support/](https://ShohTagawa.github.io/support/)<br>
[リンク③](support/howto)：一つ下の階層への相対リンク(howto.md)。旧URLは、[https://ShohTagawa.github.io/support/howto](https://ShohTagawa.github.io/support/howto)<br>
[リンク④](support/test.jpg)：一つ下の階層の画像ファイル。旧URLは、[https://ShohTagawa.github.io/support/test.jpg](https://ShohTagawa.github.io/support/test.jpg)<br>
[リンク⑤](support/howto#2方法)：一つ下の階層の相対リンク(howto.md)中のタグ1へのリンク。旧URLは、[https://ShohTagawa.github.io/support/howto#2方法](https://ShohTagawa.github.io/support/howto#2方法)<br>

## 気になる点   
- 英語ページへのリンクなどはきちんと動くか。   <br>
- Googleのクロールは、どちらのサイトで登録されるか。   <br>
- httpsの問題はないか。   <br>

## 設定手順   
- 設定した手順については、[howto](support/howto)にのせました。<br>

## 備考
- 今回の実験例は、初期設定のミスで、Apex domainに対して、CNAMEを書く(振る舞わせる?)、若干イレギュラーな話になっています(Xserverの機能が一部入っています)。一方で、通常のdomainに対してCNAME書くのも、同じ手順で行けるはずです。<br>