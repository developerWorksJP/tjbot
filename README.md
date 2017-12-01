# IBM TJBot
<img src="images/tjbot.jpg" width="85%">

[IBM Watson Maker Kits](http://ibm.biz/mytjbot)は、[Watson](https://www.ibm.com/watson/developercloud/services-catalog.html)で楽しく簡単な方法でビルドするDIYオープンソース・テンプレートのコレクションです。[IBM TJBot](http://ibm.biz/mytjbot) は、コレクションで初めてのメーカーキットです。 3Dプリントやレーザーボディをレーザーカットした後、レシピを使って命を吹き込むことができます！
さらに、独自の創造性を発揮し、利用可能な[Watsonサービス](https://www.ibm.com/watson/developercloud/services-catalog.html)を使用してTJBotに新しい[recipes](recipes)を作成することができます。

**TJBotはラズベリーパイでのみ動作します。**

# TJBotを作る
さまざまな方法で独自のTJBotを作ることができます。

- **３Dプリンタまたはレーザーカット**：3Dプリンタやレーザーカッターにアクセスできる場合は、TJBotを印刷したり、カットしたりすることができます。 まず、[デザインファイル](https://ibmtjbot.github.io/#gettj)をダウンロードし、プリンタ/カッターを起動します。
- **TJBotフルキット**：  [Sparkfun](https://www.sparkfun.com/products/14123)、[Adafruit](https://www.adafruit.com/product/3462)、もしくは[Robotkingdom](http://shop.robotkingdom.com.tw/raspberry-pi/tjbot01.html)のレーザーカットボール紙とすべての電子機器で、完全なTJBotキットをオーダーすることができます。
- **TJBotカードボードキット**：[Texas Laser Creations](http://texlaser.com)からTJBotレーザーカット厚紙を購入することができます。


## エレクトロニクス
TJBotを動かすために追加可能な様々なコンポーネントがあります。すべてのレシピにこれらのすべてが必要というわけではありません。

- [Raspberry Pi 3 + NOOBSがプリロードされたSDカード](http://www.mcmelectronics.com/product/RASPBERRY-PI-RPI-MODB-16GB-NOOBS-/83-17304). **これはTJBotを動作させるために必要なコンポーネントです！** 🤖
- [NeoPixel RGB LED (8mm)](https://www.adafruit.com/product/1734)：他の種類のLEDを使用している場合は、レジスターを追加する必要があります。このLEDは1つを必要としません。
- [メス - メスジャンパーワイヤー](https://www.amazon.com/dp/B00KOL5BCC/)：TJBotはこれらのワイヤーのうちの3つだけを必要とするので、余分なものがあります。
- [メス-オスのジャンパーワイヤー](https://www.amazon.com/dp/B00PBZMN7C/)：TJBotはこれらのワイヤーのうちの3つだけを必要とするので、余分なものがあります。
- [USBマイク](https://www.amazon.com/gp/product/B00IR8R7WQ/)：他のブランドのUSBマイクも動作するはずです。
- [ミニBluetoothスピーカー](https://www.amazon.com/gp/product/B00OEPCHL2/)：3.5mmオーディオジャックまたはBluetoothのいずれかの小型スピーカーが動作します。 3.5mmオーディオジャックを使用している場合は、[USBオーディオアダプタ](https://www.adafruit.com/product/1475)を追加して、LEDによるオーディオの干渉を避けることができます。
- [サーボモーター](https://www.amazon.com/RioRand-micro-Helicopter-Airplane-Controls/dp/B00JJZXRR0/)：赤（中）のワイヤは5V、茶色のワイヤはグラウンド、オレンジのワイヤはデータです。

- [Raspberry Pi Camera](https://www.amazon.com/dp/B01ER2SKFS/)：5MPまたは8MPカメラのいずれかが動作します。


## アセンブリ
TJBotを入手したら、[アセンブリ説明書](http://www.instructables.com/id/Build-TJ-Bot-Out-of-Cardboard/)を参照ください。
参考までに、ここではLEDとサーボをRaspberry Piに接続する配線図は次の通りです。



![](images/wiring.png)

> 💡 LEDを接続するときはご注意ください！ 間違った方法で接続されると、燃える可能性があります。 LEDは一方の面に平坦なノッチを有します。これを使用してLEDの向きを確認し、どのピンがどれであるか把握します。

> サーボの場合は、赤（中）のワイヤが5V、茶色のワイヤがグラウンド、オレンジのワイヤがデータであることに注意してください。

# TJBotを動かす
まず、TJBot用にRaspberry Piを設定していることを確認します。 そのコマンドを実行してTJBotをダウンロードしてインストールしてください：

```
curl -sL http://ibm.biz/tjbot-bootstrap | sudo sh -
```

[レシピ](recipes)では、[Watson](https://www.ibm.com/watson/developercloud/services-catalog.html)でTJBotを動かすためのステップ by ステップの手順を説明しています。

3つの初期 [レシピ](recipes)をご紹介しています:

- ワトソンで光を制御するためにあなたの声を使用する [[説明](http://www.instructables.com/id/Use-Your-Voice-to-Control-a-Light-With-Watson/)] [[github](https://github.com/ibmtjbot/tjbot/tree/master/recipes/speech_to_text)]
- ワトソンを使ってあなたのロボットが感情に反応するようにする[[説明](http://www.instructables.com/id/Make-Your-Robot-Respond-to-Emotions-Using-Watson/)] [[github](https://github.com/ibmtjbot/tjbot/tree/master/recipes/sentiment_analysis)]
- ワトソンと話すロボットを作る [[説明](http://www.instructables.com/id/Build-a-Talking-Robot-With-Watson-and-Raspberry-Pi/)] [[github](https://github.com/ibmtjbot/tjbot/tree/master/recipes/conversation)]

サンプルレシピをチェックした後、コミュニティのメンバーが作成した[レシピ](featured)もご覧ください。 

# TJBotに貢献する
TJBotは、[Watson](https://www.ibm.com/watson/developercloud/services-catalog.html)と楽しく簡単にやりとりできるように設計されたオープンソースプロジェクトです。まず、始めるため役立つアイデアをご紹介します。

- **Visual recognition**：[Watson Visual Recognition](https://www.ibm.com/watson/developercloud/visual-recognition.html) サービスとRaspberry Pi カメラを使用して、TJBotがあなたの顔を認識できるようにします。
- **IoT**.：TJBotが[Watson IoTプラットフォーム](https://www.ibm.com/internet-of-things/platform/watson-iot-platform/)を使用してスマートホームデバイスを制御できるようにします。
- **Connected robots**：複数のTJBotとチャットできるようプログラムしましょう。

あなたのレシピを[レシピ](featured)のリストに掲載したい場合は、レポジトリへのリンクとデモビデオを[eメール](mailto:tjbot@us.ibm.com)でお送りください。
 

# TJBotについて
[TJBot](http://ibm.biz/mytjbot)は、IBMの初代 会長兼最高経営責任者（CEO）であるトーマス・J・ワトソンの名称にちなんで命名され、IBM Researchの[Maryam Ashoori](https://github.com/maryamashoori)によって、コグニティブな物体の設計と実装におけるベストプラクティスを見つけるための実験として作成されました。 TJBotは[このブログ](https://www.ibm.com/blogs/research/2016/11/calling-makers-meet-tj-bot/)の投稿を通じて2016年11月9日に誕生しました。

ご不明な点があればお気軽に[チーム](mailto:tjbot@us.ibm.com)にご連絡ください（TJBotに関する技術的な問題を除き）。 技術的な問題については、こちらに[issue](https://github.com/ibmtjbot/tjbot/issues)としてご記入願います。


# ライセンス
このプロジェクトでは、[Apache License Version 2.0](LICENSE) ソフトウェアライセンスを使用しています。
