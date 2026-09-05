# システム仕様
プレイヤーがフィールドから脱出する際のシステム。
- 簡単に作れる
- ユーザーからして分かりやすく
- ランダム性を作る 
ことを意識している。
脱出可能地点に10カウント滞在することでロビーに戻りアイテムを売却したりアイテムを購入、または鑑定を行い次の探索に備えさせる。

---
## 脱出可能地点について
脱出可能地点を
- エメラルドブロック 
- ダイヤモンドブロック 
- 石炭ブロック 
- 金ブロック 
- ラピスブロック
とし、それぞれに対応する`score`をランダムに抽選。
`score`がそれぞれ1となった時のみ脱出可能地点としている。
> 制限時間が0になった時に抽選させる。
---
## 脱出可能地点に滞在することで脱出
脱出可能地点のブロックの上にいる時20ティック毎にカウントを1増やす。
- カウントが10になったとき脱出。
> どの脱出可能地点にも滞在していないが、カウントが1以上ある場合15tick毎にカウントを1減らす。
---
## 前提コマンド
- scoreboard objective add exitpt dummy
- scoreboard objective add lapis duwwy
- scoreboard objective add diamond dummy
- scoreboard objective add coal dummy
- scoreboard objective add emerald dummy
- scoreboard objective add gold dummy
