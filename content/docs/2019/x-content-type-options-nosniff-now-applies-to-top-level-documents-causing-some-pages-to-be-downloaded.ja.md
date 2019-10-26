---
title: "`X-Content-Type-Options: nosniff` がトップレベルドキュメントにも適用されたことで、一部のページがダウンロードされてしまいます"
date: "2019-10-21T19:11:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["71"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1580607"
      title: "Bug 1580607 - Logout from Office365 causes download dialog box"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1582671"
      title: "Bug 1582671 - Firefox Treats Arris Modem Webpages (application/x-unknown-content-type) As Files to Download"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587448"
      title: "Bug 1587448 - Enable XTCO-nosniff for FF 71"
---
[`X-Content-Type-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Content-Type-Options) HTTP レスポンスヘッダーは Firefox 50 以降使用可能となっており、その `nosniff` ディレクティブを使うことで、間違った MIME タイプで配信されているスクリプトやスタイルシートを効果的にブロックすることができます。

Firefox 71 以降、ブラウザーセキュリティのさらなる向上を目的として、この対応がトップレベルドキュメントにも適用されます。つまり、`X-Content-Type-Options` ヘッダーが活用されている場合、`text/html` 以外の MIME タイプで配信された HTML ウェブページは、レンダリングされる代わりにダウンロードされることになります。

*Microsoft Office 365* を含め、この変更の影響を受ける既知のサイトがいくつかあるため、あなたのサイトも必ず再確認しましょう。