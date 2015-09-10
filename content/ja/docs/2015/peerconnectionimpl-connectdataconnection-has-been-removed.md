---
title: "`PeerConnectionImpl.connectDataConnection` が削除されました"
date: "2015-01-16T09:37:54-05:00"
categories: ["webrtc"]
tags: []
versions: "37"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1110478": "Bug 1110478 – Remove unused remnants of non-standard connectDataConnection from Bug 852908"
---
Firefox 22 以降廃止予定で no-op (何もしない) となっていた非標準メソッド [`PeerConnectionImpl.connectDataConnection`](https://hacks.mozilla.org/2012/11/progress-update-on-webrtc-for-firefox-on-desktop/) が削除されました。開発者はもはやこのメソッドを使用する必要はありません。