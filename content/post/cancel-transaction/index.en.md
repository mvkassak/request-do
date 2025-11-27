---
title: Unlocking Sessions with a Single Command
description: 
date: '2023-12-03'
categories:
    - Quick tips
tags:
    - Session
---

Have you ever been stuck mid-action in ServiceNow, with the whole session frozen and unresponsive?  Yeah, me too — especially when running shady scripts in the background...  

## What is `cancel_my_transaction.do`?

It’s basically a "get out of jail free" card for frozen sessions.  
When ServiceNow locks up — usually because of a long-running transaction — this command tells the platform to cancel whatever is stuck, so you can get back to work without needing to refresh or log out.

## How to Use It

Super simple:

- Take your current ServiceNow URL and add `/cancel_my_transaction.do` at the end.
- Hit Enter, and that’s it — your session should unlock almost instantly.

Example:  
`https://yourinstance.service-now.com/cancel_my_transaction.do`

## A Few Things to Watch Out For

Before you make this part of your regular toolkit, a quick heads-up:

- **You might lose unsaved work.**  
  If you cancel a transaction that was in the middle of saving or processing data, that work is gone.
- **It can interrupt workflows.**  
  If your frozen session was tied to a bigger process (like an approval flow or background script), canceling it might have ripple effects.

So yeah — use it when you need it, but use it thoughtfully.

## Final Thoughts

`cancel_my_transaction.do` is one of those low-key lifesavers that every ServiceNow user should know about.  
It’s not magic, but when you’re stuck and don’t want to lose your momentum, it can feel pretty close.

---
