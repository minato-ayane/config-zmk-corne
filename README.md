j## bluetooth対応ロータリーエンコーダ付きcorne
- フォームウェアにZMKを使用
- 5個のbluetooth接続プロファイルを保持
- 有線接続にも対応。
- LiPoバッテリーを搭載し、繰り返し充電可能 
- ロータリーエンコーダ搭載


## 電源スイッチ
- 電源スイッチは下記写真の〇印の箇所にあります。上がON,下がOFFです。
<img width="544" alt="sw" src="./doc/sw.png">


## LED点灯
- LEDは下記写真の〇印の箇所にあります。
 <img width="544" alt="led" src="./doc/led.png">

- 電源投入時に２度点滅します
- 1回目　バッテリー残量　グリーン：100～80％　　イエロー：80～20％　　レッド：20～0％
- 2回目　bluetooth接続状態　　ブルー：接続完了　　イエロー：未設定　　　レッド：未接続

## キースイッチ変更時の注意点
- バッテリーはミドルプレートとボトムプレートの間に保持されています。![image](./doc/battery.jpg)
ミドルプレートはスペーサーによる支持はされていないため、無理に上から押さえつけるようにキースイッチを取り付けると、ミドルプレートが押し下げられて、バッテリーに負担がかかってしまいます。次の図のように、キースイッチの足がソケットに浅くしかかかっていないと、その分だけミドルプレートが押し下げられて、バッテリーに負担がかかってしまいます。
![image](./doc/keyswitch_miss.jpg)
- 対策としては、一旦トッププレートのみを取り外して、トッププレートの４隅にキースイッチを取り付けた後にミドルプレートへキースイッチの足を差し込むようにしてください。 
![image](./doc/top_plate1.jpg)
![image](./doc/top_plate2.jpg)
その後は、ミドルプレートが押し下げられないよう気を付けつつ、キースイッチを１つずつはめ込んでいってください。


## 特記事項
- 充電する際は、スイッチONの状態で行ってください。
- 左手キーボードはバッテリー充電中にbluetoothとデバイスとの接続が遮断されます。充電しながらキーボードを使用したい場合は、使用するデバイスと有線接続で利用して下さい。他のデバイスやコンセントで充電している間は使用不可となります。
- bluetooth接続プロファイルはキーボード上で選択、削除ができます。
- PCの設定はUS配列を推奨します。日本語配列にて使用すると、記号など設定したキーと異なる出力がされてしまうことがあります。
- デフォルトキーマップとしてフォームウエアをuf2フォルダに保管しています。
- フォームウエアの変更時にBluetoothの接続に不調があれば、一旦uf2フォルダに保管してある`settings_reset-seeeduino_xiao_ble-zmk.uf2`を書き込んでみてください。



## キーマップの変更方法
- githubにログインしてください。アカウントをお持ちでなければ作成してください。
- このリポジトリをフォークして、自身のリポジトリとしてください。
- 初回のみ、Actionsを開いて次のボタンをクリックしてください。![image](./doc/action.png)
- [キーマップエディタ](https://nickcoutsos.github.io/keymap-editor/)でgithubと連携後、キーマップを変更し、saveボタン![image](./doc/save.png)を押してください。
- 5分程度経過するとフォームウェアの生成が完了しますので、![image](./doc/dl.png)このボタンをクリックしてください。
- 画面下部へスクロールして `firmware.zip`をダウンロード及び解凍してください。
- キーボードをPCとUSBケーブルで接続し、写真の〇印にリセットボタンがあるので、ダブルクリックしてください。<img width="544" alt="reset" src="./doc/reset.png">
- リセットボタンを押すことに慣れれば、爪楊枝やピンセット等を使用してカバーを外さずにダブルクリックができるようになります。しかし、最初はカバーを外して、そのカバーを使用してリセットボタンをクリックすることをお勧めします。
- ダブルクリックに成功すると、`XIAO-SENSE`という名前でドライブが認識されるので、作成したキーマップのフォームウェアを認識したドライブに移動させます。
- 左のキーボードには`corny_left rgbled_adapter-seeeduino_xiao_ble-zmk`、右のキーボードには`corny_right rgbled_adapter-seeeduino_xiao_ble-zmk`をドライブに移動させます。
- 数秒間でファイルの書き込みは終了し、書き込みに成功するとＰＣとの接続が勝手に解除され、フォルダは閉じられます。
- macにて書き込み操作をすると、エラーコード　‐36　等が上がりますが、無事書き込めています。
- 左右それぞれの書き込みが完了したら、キーマップが変更されていることを確認してください。

  ## デフォルトレイヤーの一覧
- ロータリーエンコーダの押し込みも１つのキーとして認識されます。例えば、初期レイヤ―では左手のロータリエンコーダは、取り消し,やり直しが登録されていますが、押し込みながら操作するとことでブラウザでの進む，戻るの操作が可能となっています。
- コンボという2キー以上の同時押しによるキー割り当てがあり、D,F同時押しで半角英数字入力J,K同時押しでひらがな入力としています。
- レイヤー2にbluetooth設定のキー配置をしています。BT_SEL0～4の切り替えで接続先デバイスの切替が可能で、BT_CLTにてプロファイル削除が可能です。

- 初期レイヤー
![image](./doc/332077942-19bf16c6-8f26-4089-8299-4e8c92263105.png)
- レイヤー1
 ![image](./doc/332078468-d885dab9-d509-4021-90a8-4b634ad9ac0a.png)
- レイヤー2
![image](./doc/332078632-b706e26e-55e8-479e-93d3-bed3732f5396.png)
- レイヤー3
![image](./doc/332078792-f80cbc93-9624-4e2d-8153-3cf302c16538.png)
- 英数
  
![image](./doc/332079123-b6547a28-0012-4da0-9296-b720e02214eb.png)
- かな
  
![image](./doc/332079271-80ae9fe0-c29c-4573-8757-47135ff50db9.png)
- テンキー(レイヤー3)移行
  
![image](./doc/332079567-9f1cab6e-a79e-4b27-8951-072442dd310e.png)
