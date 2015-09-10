---
title: "`XMLHttpRequest.setRequestHeader` implementation has been fixed to comply with the spec"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: "21"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=819051": "Bug 819051 – XMLHttpRequest.setRequestHeader() overwrites instead of combines values for the same header."
---
Previously, if the same headers were repeatedly set with [`XMLHttpRequest.setRequestHeader`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest#setRequestHeader), the last-specified value was used. This behavior has been changed to comply with the spec, so those values will be properly combined.