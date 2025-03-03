# 第13回 NET分野実習　2022年9月7日

## 無線通信

### 無線通信を行っているもの
* 会話
* 狼煙
* 手旗信号
* PC
* FM/AMラジオ 
* テレビのリモコン etc.


### 通信媒体
* 電気
* 光  
→ どちらも **電磁波**


### 電磁波に関連する学問
* 電磁気学  
  工学部は必修
* 光学
* 量子力学

### 電磁波とは
* 光も電波も可視光も電磁波
* 違いは波長の違い
* 波長が長いと赤外線となり、短いと紫外線となる

```
[波長/長]ガンマ線 → X線 → 紫外線 → 可視光線 → 赤外線 → レーダー → テレビ/FMラジオ → 短波 → AMラジオ[短]
```

### 通信に利用される電磁波
* 赤外線(カメラで見られる)
* 電波
* 可視光を使った通信技術もある

### 赤外線通信
* IrDA
* 通信は1対1のみ
* 短距離の見通し通信(遮蔽物なし)
* 反射により、範囲を拡大できる(鏡に反射する)

### Radio Frequency(RF)
* 遮蔽物があっても回折・貫通等で通信可能
* 無線LAN、コンピューター周辺機器などで使用される
* 小電力無線局は技適があれば使用可能
* **ISMバンド**であれば制限なく使用できる

### Bluetooth
* 2.4Hz帯域を使用する
* 短距離の通信に制限されるが１対多の通信が可能
* 消費電力が少ない
* AirDropなどもBluetoothを使用している

### 問題
[IR(赤外線)] [RF(無線周波数)] [Bluetooth] のどれか
1. PCを公共の**無線LAN**につなぎ、電子メールをチェックする  
  → `RF(無線周波数)`

2. ヘッドフォンを使用してハンドフリー通話をする  
  → `Bluetooth`

3. **ガラケー**を使用して写真交換を行う  
  → `IR(赤外線)`

4. 上の階の音楽プレイヤーから、コードレスヘッドフォンを使用して**3階下**で音楽を聞く  
  → `RF(無線周波数)`

5. **無線デバイス3つ**を、デスクトップPCに接続する  
  → `Bluetooth` (`RF(無線周波数)`)  
  独自規格のRFの可能性もある

6. コードレス電話機は**5.8GHz帯域**を使用していた  
  → `RF(無線周波数)`

#### FMラジオとAMラジオ
* 波長 FM < AM
* FM の方が回析(回り込み)しやすい
* AM の方が貫通しやすい
* 波長が長いほど遠くまで届く
* 波長が長さ = アンテナの長さ

#### 無線テクノロジーのメリット
* 時間・場所を選ばない
* 初期設定が簡単
* ケーブルの制限を受けない


#### 無線テクノロジーの特徴
* 2.4GHz帯域は `ISMバンド` により制限を受けない
* ただしさまざまな機器が使用しているため輻輳状態となり、干渉する
* 電磁波だかた誰でも盗聴可能  
  → **暗号化**や**認証**の仕組みが必須

#### 電波に関する法律
* 電波を扱う機器は**電波法**の制限を受ける
* 電波法は国によって内容が異なる
* 電気通信を利用して提供されるサービスに対して**電気通信事業法**がある
* 日本では**技適マーク**がなければ無線通信機器は販売できない

#### 無線ネットワークの種類と境界
* WWAN
  * 携帯電話ネットワークなど
* WLAN
  * 無線LAN IEEE802.11規格
* WPAN

#### IEEE802.11規格
* 無線LANの規格の一つ
* これ以外の規格はあるが主流はこれ
* IEEE802.11 の中で新しい規格が追加されている
* 現在のスマホの多くは `802.11ac` が多い
* 最大伝送速度は理論値(早くてもケーブルが...とか)

#### 無線LANコンポーネント
* 無線LANクライアント
  * 接続する端末
* アクセスポイント
  * 無線LANに接続するための中継点となる端末
* 無線ブリッジ
  * 範囲を拡張するためのブリッジ
* アンテナ
  * 無線デバイスからの出力信号の強度を増加する

#### アンテナ
* 指向性アンテナ
  * 信号強度を一方向に集中させる
  * 代表例 `八木アンテナ`
* 無指向性アンテナ
  * AP上で多く使用される

<br>

## メモ

### サイバー攻撃
**DDoS攻撃**  
* 攻撃手法の一つ
* BOTネットを使っているものは深刻
  * 世界の一般コンピューターを従えて同時に攻撃
* DDoS攻撃サービスもある

<br>

## 感想
FMとAMの違いを知らなかったが、AM,FMは変調のことで飛ばす電波の波形が違うことが分かった。
普通は片方が生き残ると思うが、両方利用されてるという点でどちらも優越つけ難いのだろうと思った。

昔の家には八木アンテナが乗っていて最近はパラボラアンテナが多いイメージだったが、八木アンテナの性能が劣っているのではないかと思った。しかし調べてみると細くて折れやすかったり屋根の上に付ける必要があるなどの扱いやすさが問題だと分かった。性能が良くても扱いやすくなければ普及しないという事が分かり、何かシステムを作る上でも大切だと思った。
