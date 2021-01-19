---
title: テストページ
---

このページは、GitHub Desktopで作成したページが、別のdomainへ転送出来るのかを試すために使われyたものです。
処理としては、CNAMEを書いただけです。
[基本的にはこちら](https://docs.github.com/ja/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#%E3%82%B5%E3%83%96%E3%83%89%E3%83%A1%E3%82%A4%E3%83%B3%E3%82%92%E8%A8%AD%E5%AE%9A%E3%81%99%E3%82%8B)を参照しています<br>

## テストの方法
アドレスを転送する上で、もっともネックになるのは、既存ページの一部に対するリンクが動かなくなることです。
下記は、リンクが動くかのテストです
[リンク①](what_not_new)：おなじ次元の相対リンク
[リンク②](support/index)：一つ下の次元の相対リンク
[リンク③](support/test.jpg)：一つ下の画像ファイル

## 気になる点
- 英語ページへのリンクなどはきちんと動くか?
- Googleのクロールは、どちらのサイトで登録されるか。
- httpsの問題はないか