---
title: "Obsidian dataviewでfuzzy関連ファイルサーチをするクエリ"
type: ""
description: ""
preview: ""
created: 2025-08-18T06:35:47.984Z
updated: null
tags: memo
keywords: []
fmContentType: memo
---
「何故今更dataview？もう時代はobsidian basesだよ」？
うるさいなぁ、再現できないんだよ

## 何ができるの
- ファイル名・プロパティのaliasesを見て、そのテキストをファイル名・プロパティに含むファイルをvault全体から探してくる

## 使い方
Obsidianのコミュニティプラグインからdataviewを入れて以下のスクリプトをコピペ

### オプション
createdとupdatedは好きなプロパティに変えると良い

````
```dataview
table
	created as "作成日",
	updated as "更新日"
from ""
where icontains(file.name, this.file.name) or icontains(file.aliases, this.file.name) or any(this.file.aliases, (alias) => icontains(file.name, alias)) or (length(this.file.aliases) > 1 AND any(this.file.aliases, (alias) => icontains(file.aliases, alias)))
sort created asc
```
````