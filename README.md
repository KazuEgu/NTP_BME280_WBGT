NTPサーバから時刻を取得し、BME280より気温、気圧、湿度を取得。WBGTは近似式を使い計算。<br>
ハードは以下の通りです。<br>
マイコン: Raspberry Pi Pico W<br>
LCD: 2004AにI2CシリアルIFモジュール(PCF8574T I2Cアドレスは0x27)<br>
BME280は秋月電子で購入。I2Cで使うので、センサー基板のJ3をはんだでジャンプ。I2Cアドレスは0x76 （VDOをGNDに接続）。

envはWiFi設定ファイル <br>
WIFI_SSIDとWIFI_PASSは環境に合わせて設定が必要。

必要なパッケージ（ライブラリ）は以下の通り。<br>
bme280.py <br>
esp8266_i2c_lcd.py <br>
lcd_api.py <br>

以下のBLOGにもう少し詳細記載しています。<br>
https://kazuho-e-blog.tokyo/?p=3059

参考にさせていただいたWEBは以下の通りです。謝辞申し上げます。<br>
MicroPython:NTPとRTCを使って時計を表示<br>" https://plaza.rakuten.co.jp/washiinuru/diary/202309100000/ " <br>
Raspberry Pi Pico MicroPython BME280テスト<br>" https://blog.goo.ne.jp/jh7ubc/e/07755b250db432675611dff9f9ea1144 " <br>
温湿度センサーを使って熱中症対策デバイスを作る<br>" https://info.picaca.jp/12370 "
