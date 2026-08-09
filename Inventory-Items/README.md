# Changing Inventory Items

In *Doubutsu no Mori e+*, the items in the player's inventory can be modified by directly changing their values in memory.

## Inventory Address

The following memory location corresponds to the **second item in the inventory**:

* `0x81266D00` — **Column 2**

The value stored in Column 2 at this address determines the second item in the player's inventory.

If the player does not have an item in this position, the value is:

```text
0
```

## Changing the Second Item

By changing the value in **Column 2 at `0x81266D00`**, the second item in the inventory can be modified.

### Current State

#### Second Item in the Inventory

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/50791d46-3979-43c3-a6f2-57a7bcda288e" />

#### Memory Value

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/3ac8db81-9338-4c72-979e-a06c7caebf55" />

</br>

### After Modification

#### Modified Memory Value　「121212」

<img width="400" alt="image" src="https://github.com/user-attachments/assets/d71bafe4-bacd-417d-a690-cd9cbf90911e" />

#### Second Item After Modification

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/393e55a8-9f3e-4adc-bad1-f82720149b52" />

</br></br>

# Item List

| Value | Item Name |
| ----- | ------------ |
| 1 | 切り株 |
| 2 | 切り株 |
| 3 | 切り株 |
| 4 | 切り株 |
| 5 | 柵 |
| 6 | 透明の判定なしのアイテム |
| 7 | 掲示板 |
| 8 | 雑草 |
| 9 | 雑草 |
| 10 | 雑草 |
| 11 | 透明の判定なしのアイテム |
| 12 | 地図 |
| 13 | 透明の判定なしのアイテム |
| 14 | 曲掲示板 |
| 15 | 透明の判定なしのアイテム  |
| 16 | 柵 |
| 17 | スコップの穴 |
| ... | ... |
| 41 | スコップの穴? |
| 42 | 落とし穴の種が埋まったもの |
| ... | ... |
| 66 | 落とし穴の種が埋まったもの? |
| 67 | 埋まったもの? |
| ... | ... |
| 91 | 埋まったもの? |
| 92 | 光る埋まったもの |
| 93 | 穴 |
| 94 | 蜂の巣ありの木 |
| 95 | アイテムが落ちてくる木 |
| 96 | 普通の木 |
| 97 | プレゼントが落ちてくる木 |
| 98 | 蜂の巣(すぐ消える) |
| 99 | 普通の岩 |
| 100 | 普通の岩 |

| Value | Item Name |
| ----- | --------- |
| 101 | 普通の岩 |
| ... | ... |
| 104 | 普通の岩? |
| 105 | お金が落ちてくる木 |
| 106 | お金でる岩 |
| ... | ... |
| 110 | お金でる岩 |
| 111 | 透明のお金でる岩 |
| 112 | 切り株 |
| ... | ... |
| 119 | 切り株 |
| 120 | お金が落ちてくる木 |
| 121 | アイテムが落ちてくる木 |
| 122 | 蜂の巣が落ちてくる木 |
| 123 | 切り株 |
| ... | ... |
| 126 | 切り株 |
| 127 | お金が落ちてくる金の木 |
| 128 | アイテムが落ちてくる金の木 |
| 129 | 蜂の巣が落ちてくる金の木 |
| 130 | 普通の木 |
| ... | ... |
| 140 | 壊れる岩 |
| 141 | すでに壊れた岩 |
| ... | ... |
| 145 | すでに壊れた岩 |
| 146 | たかねのはな |
| 147 | あたり判定ない木 |
| ... | あたり判定ない木 |

| Value | Item Name |
| ----- | --------- |
| ... | あたり判定ない木 |
| 206 | あたり判定ない木 |
| 207 | 花の草部分 |
| ... | ... |
| 224 | 摘めない花 |
| 225 | あたり判定ない木 |
| ... | ... |
| 252 | あたり判定ない木 |
| 253 | 謎のもの? |
| ... | ... |

| Value | Item Name |
| ----- | --------- |
| ... | ... |
| 4095 | 謎のもの? |
| 4096 | ハロウィンクローゼット |
| 4100 | シックなクローゼット |
| 4104 | あおいクローゼット |
| 4108 | ロッカー |
| 4112 | クリスマスクローゼット |
| 4112 | クリスマスクローゼット |
| 4116 | ロイヤルなクローゼット |
| 4120 | リゾートなクローゼット |
| 4124 | ログクローゼット |
| 4128 | ラブリークローゼット |
| 4132 | みどりのクローゼット |
| 4136 | ようなしのクローゼット |
| 4140 | カントリークローゼット |
| 4144 | あおいキャビネット |
| 4148 | モノクロクローゼット |
| 4152 | アジアなクローゼット |
| 4156 | クリスマスタンス |
| 4160 | ロイヤルなタンス |
| 4164 | リゾートなタンス |
| 4168 | ログタンス |
| 4172 | ラブリータンス |




















