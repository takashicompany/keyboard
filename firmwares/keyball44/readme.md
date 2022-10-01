# Keyball44 miniZoneファームウェア

[miniZone](https://github.com/takashicompany/minizone)で開発したファームウェアの実装をcocot46plusに流用したものです。

https://user-images.githubusercontent.com/4215759/162611440-2bb0ec75-2dbf-48b8-8c0d-54c8666c1aff.mp4

上述の動画と同様にトラックボールを動かした際に一定時間、指定されたレイヤー(デフォルトでは8番目...index7のレイヤー)が有効になります。  

## ファームウェアの書き込み

ファイルは[こちら](https://github.com/takashicompany/qmk_firmware/releases/download/cocot46plus-tc-1.0.0/cocot46plus_takashicompany.hex)からダウンロードできます。

[Pro Micro Web Updater](https://sekigon-gonnoc.github.io/promicro-web-updater/index.html)や[QMK Toolbox](https://kbd.dailycraft.jp/claw44/buildguide/10_firmware/toolbox/)でファームウェアをPro Microに書き込んでください。

または、[当ブランチ](https://github.com/takashicompany/qmk_firmware/tree/cocot46plus/takashicompany/)を `git checkout` するかダウンロードした後に、以下のコマンドを実行することでファームウェアのビルドと書き込みが可能です。

```
make cocot46plus:takashicompany:flash
```

(Remapからの書き込みは後日に　設計者さんに依頼する予定です)

## Remapでのマウスキーの書き込みについて

当ファームウェアはRemapに対応しております。  
レイヤー数は7となります。

<img src="https://user-images.githubusercontent.com/4215759/180040883-020505fd-9e27-468f-ae4c-ebdc705c51d3.png" width="800px"/>


|キー|Code(hex)|説明|
|:--|:--|:--|
|マウスボタン1|0x5DAE|主に左クリックが設定されていることが多い。|
|マウスボタン2|0x5DAF|主に右クリックが設定されていることが多い。|
|マウスボタン3|0x5DB0|OSやPCの設定に依存。|
|スクロールボタン|0x5DB1|このキーを押している際はトラックボールの入力はスクロールとして扱われる。|

## その他

- 当ファームウェア、ソースコードを使用したことでの不利益や故障などは責任は負いかねます。