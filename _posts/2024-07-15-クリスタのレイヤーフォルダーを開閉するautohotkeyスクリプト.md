---
type: memo
description: "クリスタのレイヤーフォルダーを開閉するahkスクリプト"
preview: ""
created: 2024-07-14T17:43:42.166Z
updated: 2024-07-14T17:43:42.167Z
tags: memo
keywords: []
---
[レイヤーフォルダ開閉をショートカットで行いたいです | CLIP STUDIO PAINTのみんなに聞いてみよう | CLIP STUDIO](https://www.clip-studio.com/clip_site/support/help/detail/svc/53/tid/72515)
絶望、ということで作りました

みんなが欲しかったのはこれだよな？

## 使い方
- 1行目F20の部分を任意のキーに置き換えて
- 2行目hoge, fugaをレイヤーキャンバスタブのチェックボックスのすぐ左、
- 2行目piyo, hogera,をその右下の座標に置き換える
（説明がむずいので需要があれば連絡してもらえばちゃんと説明する）

クリスタ公式がしっかりしてくれればこんなもん作らなくてすむのに

```
    F20::
        PixelSearch, posX, posY, hoge, fuga, piyo, hogera, 0x614c42, 0, Fast
        if (ErrorLevel == 0) ; 色が見つかった場合
        {
            ; 色が見つかった位置をクリック
            CoordMode, Mouse, Screen
            MouseClick, L, %posX%, %posY%, 1, 0,
        } ; 見つからなかった場合
        else if (ErrorLevel == 1)
        {
            MsgBox, 色 #424c61 は見つかりませんでした。
        }
        Else{ ;エラーのとき
            MsgBox, error
        }
    Return
```

