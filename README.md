NTPサーバから時刻を取得し、BME280より気温、気圧、湿度を取得。WBGTは近似式を使い計算。
LCDは2004AにI2CシリアルIFモジュール(PCF8574T I2Cアドレスは0x27)を使用。
BME280は秋月電子で購入。I2Cで使うので、センサー基板のJ3をはんだでジャンプ。I2Cアドレスは0x76 （VDOをGNDに接続）。

envはWiFi設定ファイル
WIFI_SSIDとWIFI_PASSは環境に合わせて設定が必要。

必要なパッケージ（ライブラリ）は以下の通り。
bme280.py
esp8266_i2c_lcd.py
lcd_api.py

参考にさせていただいたWEBは以下の通りです。深謝いたしますとともに、謝辞申し上げます。<br>
MicroPython:NTPとRTCを使って時計を表示 " https://plaza.rakuten.co.jp/washiinuru/diary/202309100000/ "
Raspberry Pi Pico MicroPython BME280テスト " https://blog.goo.ne.jp/jh7ubc/e/07755b250db432675611dff9f9ea1144 "
温湿度センサーを使って熱中症対策デバイスを作る " https://info.picaca.jp/12370 "
