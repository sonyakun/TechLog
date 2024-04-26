---
title: ActivityPub実装に関するメモ
date: 2023-12-23T19:00:00.000Z
categories:
    - memo
tags:
    - activitypub
    - python
    - fastapi
slug: activitypub-memo

draft: true
links:
  - title: sonyakun/Leaf
    description: 作成中のActivityPubサーバー。Misskeyの仕様に準拠するつもり
    website: https://github.com/sonyakun/leaf
    image: null
  - title: ActivityPubのW3C勧告
    description: ActivityPub仕様に関するW3C勧告。
    website: https://www.w3.org/TR/activitypub/
    image: https://www.w3.org/StyleSheets/TR/2016/logos/W3C
  - title: Mastodonの実装しているActivityPub仕様
    description: Mastodonが実装しているActivityPubの仕様
    website: https://docs.joinmastodon.org/spec/activitypub/
    image: https://joinmastodon.org/logos/logo-purple.svg
  - title: Misskey Extensions to ActivityPub
    description: Misskeyが実装しているActivityPubの拡張仕様 (独自仕様)
    website: https://misskey-hub.net/ns/
    image: https://assets.misskey-hub.net/public/icon.png
---
個人的にPythonでActivityPub実装を書いてるのでメモ用に。