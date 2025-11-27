---
title: A simple way to unlock a frozen session
description: 
date: '2023-12-03'
categories:
    - Quick tips
tags:
    - Session
---

Have you ever had a browser tab freeze in the middle of something in ServiceNow? It usually happens when a script takes longer than expected or a form tries to process more than it should. The page stops responding, and you sit there wondering if you should refresh or open incognito.

There’s a small command that can save you in these moments: `cancel_my_transaction.do`.

## What it does

When your session gets stuck, ServiceNow is usually busy running a transaction in the background. This endpoint tells the platform to stop whatever is running so the session can recover. No need to reload the whole page or log in again.

## How to use it

- Take the URL of the tab that froze.  
- Add `/cancel_my_transaction.do` at the end.  
- Press Enter.  

Example:  
`https://yourinstance.service-now.com/cancel_my_transaction.do`

If the issue was caused by a long-running transaction, the session unlocks right away.

## Before you rely on it

There are a few things to keep in mind:

- Canceling a transaction can drop any work that wasn’t saved.  
- If the action was part of a bigger process, stopping it might leave that process incomplete.  
- It’s a recovery tool, not something you should use to skip slow operations on purpose.

## Closing thoughts

This little endpoint won’t solve every freeze, but it helps when you’re stuck and don’t want to start over. It’s a small trick that makes life easier when you work on the platform every day.
