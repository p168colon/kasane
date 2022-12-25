# kasane

![kasane01](/images/kasane01.jpg)
アクリル積層ケースのマクロパッドです。

* [販売ページ](https://p168colon.com/products/kasane)

## ビルドガイド

### セットに含まれるもの
* PCB 1枚
* アクリルケース（ネジ、スペーサーなど含む） 1式
* タクトスイッチ（リセットスイッチ用。） 1つ
* ダイオード（1N4148W 5つ。１つは予備です。）
* ピンヘッダ 2本
* ピンソケット 2本
* 滑り止めフェルト 1枚

### セットのほかに必要なもの
* お好きなMX スイッチ 4つ（※5本足を推奨）
* Pro micro 1つ
* お好きなキーキャップ 4つ
* お好きなマイクロUSBケーブル 1本

### 1.セット内容の確認
まずセット内容を確認します。以下揃っていますでしょうか。
* 1〜7の番号がふられたアクリルが7枚
* 2番のアクリルにネジ止めされたPCB1枚
* PCB下にパッキングされた部品
* アクリルケース下に敷かれた滑り止めフェルト

![kasane_build_01](/images/kasane_build_01.jpg)

確認できたら、アクリルの保護紙（もしくは保護フィルム）を剥がしておきます。
（2番の下側はすでに剥がし済みです。）
アクリルは1〜6はマットな面が上、7だけが下です。基本的にナンバーが書いてあった面が上になりますので、剥がした後は裏表逆にならないよう、元のように重ねておくと混乱しにくいと思います。
尚、4〜6についてはお好きなように並べ替えていただいて大丈夫です。

PCBはアクリルから外しておきます。
![kasane_build_02](/images/kasane_build_02.jpg)

### 2.ダイオード取り付け

ダイオードをハンダ付けします。
PCB上の「・」のある側にダイオードの線がくるようにします。1と3が上、2と4は下になっていますので間違えないようお気をつけください。
![kasane_build_03](/images/kasane_build_03.jpg)

### 3.ProMicro取り付け

ピンヘッダをソケットに差し込みます。
![kasane_build_04](/images/kasane_build_04.jpg)

ピンヘッダ側にProMicroを写真の向きで差し込み、ハンダ付けします。
ブレッドボードに差し込みながらだとずれにくいです。
![kasane_build_05](/images/kasane_build_05.jpg)

PCBにハンダ付けします。
（※この「kasane」ですが開発中は「kogara」と呼んでおり、名残がPCBに残ってしまっています…）
![kasane_build_06](/images/kasane_build_06.jpg)

一旦、ソケットからピンヘッダ＋ProMicroを外しておきます。
![kasane_build_07](/images/kasane_build_07.jpg)

### 4.スイッチ取り付け

キースイッチとリセットスイッチをハンダ付けします。
![kasane_build_08](/images/kasane_build_08.jpg)
キースイッチがズレやすい場合、マスキングテープなどで仮止めすると良いです。
![kasane_build_09](/images/kasane_build_09.jpg)

3.で外してあったProMicroは再度セットしておきます。

### 5.ケース組み立て

2番のアクリルにPCBをねじ止めします。
混乱したら、下記を確認しつつ進めてください。
* アクリルのマット面を上に
* ケース固定用のスペーサー穴が左、右上、右下に来る向きに
* PCBを下側から当ててねじ止め

![kasane_build_10](/images/kasane_build_10.jpg)

1番アクリルを上に乗せ、3箇所をボルトで止めます。
![kasane_build_11](/images/kasane_build_11.jpg)
リセットスイッチのボタン部分がケース下に入り込んでしまわないよう気をつけてください。
![kasane_build_12](/images/kasane_build_12.jpg)

ケースの底にフェルトを貼ります。
![kasane_build_13](/images/kasane_build_13.jpg)

### 6.ファームを焼く

デフォルトキーマップはアローキーになっています。
このリポジトリに「p168colon_kasane_default.hex」として置いていますので、QMK Toolboxなどで書き込んでいただけます。
リセットボタンは、トッププレートの隙間から細長いもの（爪楊枝など）を差し込んで押してください。

カスタマイズしたい方は、下記にファームの雛形がありますのでご利用ください。
https://github.com/hachi868/qmk_firmware/tree/feature-kasane/keyboards/p168colon/kasane