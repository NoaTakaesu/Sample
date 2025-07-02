### フローチャート

```mermaid
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```

<br>

#### memo 1. 

`flowchart TDはフローチャートの記載を宣言し、TDはTop⇒Downの方向にノードを並べるという意味。ほかにもLR,RL,BT(Bottom To Top)がある`

`A[Christmas]:四角形ノードの作成`<br>
`B(Go shopping):丸ノード`<br>
`-->:矢印`<br>
`|Get money|:矢印にラベルを表示`<br>
`C{Let me think}:ひし形の条件分岐ノードの作成`<br>
`F[fa:fa-car Car]：Font Awesomeアイコン付きノード`


<br>

```mermaid
graph TD
    A-->B;
    A-->C;
    B-->D;
    C-->E;
```

<br>

```mermaid
flowchart LR
A(start) ---> B
B(Click yahoo) ---> C
C(Click Google) ---> D(End)
click B "https://www.yahoo.co.jp"
click C "https://www.google.com"
```

```mermaid
flowchart LR

A(start) ---> B
B(Click yahoo) ---> C
C(Click Google) ---> D(End)
B ---> E(No Click)
E ---> D

click B "https://www.yahoo.co.jp"
click C "https://www.google.com"
click E "https://example.com/"
```

## シーケンス図

```mermaid
sequenceDiagram

participant 太郎
participant 花子
太郎->>花子: こんにちは、花子さん。元気ですか？

loop Healthcheck
花子->>花子: Fight against hypochondria
end

Note right of 花子: Rational thoughts <br/>prevail!
花子-->>太郎: 良いですよ！
花子->>次郎: あなたはどうですか？
次郎-->>花子: とてもいいです。
```

<br>

## ガントチャート

```mermaid
gantt
dateFormat YYYY-MM-DD
title ガントチャートのサンプル
excludes weekdays 2014-01-10

section A section
完了したタスク :done, des1, 2022-07-06,2022-07-08
アクティブなタスク :active, des2, 2022-07-09, 3d
未来のタスク :des3, after des2, 5d
別な未来のタスク :des4, after des3, 5d
```

<br>

#### memo 2.

`gantt:ここからシーケンス図を描き始める宣言`<br>
`dateFormat YYYY-MM-DD:日付の表示形式の指定`<br>
`excludes weekdays 2014-01-10:特定の日付を除外、excludes weekendsで土日を除外`<br>
`:done：ステータス指定(完了タスクを緑で表示)`<br>
`des1：タスクID(他のタスクから参照できる)`
`2022-07-06,2022-07-08：開始日、終了日`
`:active：進行中のタスク(青系の色で表示)`
`after des2：des2(アクティブなタスク)の終了後に開始`

<br>

## クラス図

```mermaid
classDiagram
　Class01 <|-- AveryLongClass : Cool
　Class03 *-- Class04
　Class05 o-- Class06
　Class07 .. Class08
　Class09 --> C2 : Where am i?
　Class09 --* C3
　Class09 --|> Class07
　Class07 : equals()
　Class07 : Object[] elementData
　Class01 : size()
　Class01 : int chimp
　Class01 : int gorilla
　Class08 <--> C2: Cool labe
```

<br>

#### memo 3. 

`classDiagram:- Mermaidでクラス図を描くことを宣言します。`
![alt text](image.png)



## Gitグラフ

```mermaid
gitGraph
commit
commit
branch develop
commit
commit
commit
checkout main
commit
commit
```

<br>

#### memo 4. 

![alt text](image-1.png)