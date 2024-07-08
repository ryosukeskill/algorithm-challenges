# グリッド上の最小コスト経路

この問題では、与えられたグリッド状の盤面で、上下左右の移動を繰り返して、左上のスタート地点から右下のゴール地点まで移動する際に通るマス（スタート地点とゴール地点を含む）のコストの合計の最小値を求めます。

## 問題の入力

入力は以下のような形式で与えられます。

```
h w
t_{0,0} t_{0,1} ... t_{0,w-1}
t_{1,0} t_{1,1} ... t_{1,w-1}
...
t_{h-1,0} t_{h-1,1} ... t_{h-1,w-1}
```

- 1 行目にはグリッドの高さ `h` と幅 `w` が空白区切りで与えられます。
- 2 行目からの `h` 行には、各マスのコストが空白区切りで与えられます。ここで `t_{i,j}` はグリッドの `i` 行目、`j` 列目のマスのコストを表します。

## 出力

スタート地点からゴール地点まで移動する際に通るマス（スタート地点とゴール地点を含む）のコストの合計の最小値を 1 行に出力します。

## 入力例

```
4 5
3 1 5 8 2
4 2 7 3 6
1 8 2 4 5
2 6 1 2 3
```

## 出力例

```
15
```

この場合、スタート地点からゴール地点までの最小コスト経路は `(0,0) -> (0,1) -> (1,1) -> (2,1) -> (2,2) -> (3,2) -> (3,3) -> (3,4)` であり、その合計コストは `3 + 1 + 2 + 2 + 1 + 1 + 2 + 3 = 15` となります。

## 制約

- 1 ≤ h, w ≤ 100
- 1 ≤ t\_{i,j} ≤ 1000