# PPT Address and Pointer

## ステータス類

### プレイヤー名

アドレス `0x140598BD4` を基準に 0x68 ずつ足していく

### キャラクター

アドレス `0x140598C28` を基準に 0x68 ずつ足していく  
<details>
<summary>キャラクター Byte</summary>
0:Ringo  
1:Risukuma  
2:Maguro  
3:Amitie  
4:Klug  
5:Sig  
6:Arle & Carbuncle  
7:Suketoudara  
8:Schezo  
9:Draco Centauros  
10:Witch  
11:Lemres  
12:Jay & Elle  
13:Ai  
14:Ess  
15:Zed  
16:O  
17:Tee  
18:Raffina  
19:Rulue  
20:Feli  
21:Dark Prince  
22:Ecolo  
23:Ex  
</details>

#### モードとボイスチェンジ

アドレス `0x140598C27` を基準に 0x68 ずつ足していく

<details>
<summary>中身 Byte (ほんまか？)</summary>
0:Puyo  
64:Tetris  
128:Puyo (Alt Voice)  
192:Tetris (Alt Voice)
</details>

#### ハンデ

アドレス `0x140598C1C` を基準に 0x68 ずつ足していく

<details>
<summary>中身 Byte</summary>
0:Sweet  
1:Mild  
2:Medium  
3:Hot  
4:Spicy  
プレイヤー数が増えるとずれる 実際にメモリ見て察して
</details>

### ネクスト

ポインター `0x140461B20 + 0x380 + 0x18 + 0xB8 + 0x15C` に 4 Bytes で格納されてる  
オフセット 0x4 ずつ足すとネクスト1個次 最大5個まで それ以上はRNGを解析する必要があるがまだ着手してない  
Player 2 以降 `0x140461B20 + (378 + player * 0x8) + 0xB8 + 0x15C` で取得

## ゲーム関係

この辺下手に弄るとクラッシュしやすい

### ゲームモード

アドレス `0x140598BB8` に 4 Bytes で格納されてる  

<details>
<summary>中身</summary>
1:VS: Versus  
2:VS: Crash (Fusion?)  
3:VS: Crash (Fusion?)  
4:VS: Fusion  
5:VS: Swap  
6:VS: Big Bang  
7:VS: Party  
0:Challenge: Endless Fever  
8:Challenge: Tiny Puyo  
9:Challenge: Endless Puyo  
10:Challenge: Marathon  
11:Challenge: Sprint  
12:Challenge: Ultra  
</details>

### シーン

アドレス `0x140598BB0` に 4 Bytes で格納されてる  
マジで謎が多い 調査すべき

<details>
<summary>中身</summary>
4294967295:Main Menu  
1:Solo Arcade  
2:idk, need more research  
3:Endless Puyo  
4:Endurance  
5:Title (Hidden Title Demo, Beta?)  
6:Title (Hidden Title Demo, Max level CPU)  
7:Title Demo  
8:Story 7-10  
</details>