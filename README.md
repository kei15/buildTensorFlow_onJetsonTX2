# buildTensorFlow_onJetsonTX2
JetsonTX2にTensorFlow 1.10をインストールした。

## Dependencies
* JetPack 3.2
* CUDA 9.0
* cuDNN 7.0.5
* TensorRT 3.0 GA
* Python 2.7

## Build
launchpadlibをインストールとenum34のアンインストール。これをしないと後でエラーが出た。
```
sudo pip install launchpadlib
sudo apt-get remove python-enum34
```
Python 2.7用のTensorFlow 1.10のwhlファイルを[ここ](https://nvidia.app.box.com/v/TF1100-Py27-wTRT)からダウンロードする。
**補足:** 他のバージョンをインストールする場合は[こちら](https://devtalk.nvidia.com/default/topic/1031300/jetson-tx2/tensorflow-1-11-0-wheel-with-jetpack-3-3/1)から。
そのwhlファイルがあるディレクトリで以下のコマンドを実行。
```
sudo pip2 install tensorflow-1.10.0-cp27-cp27mu-linux_aarch64.whl
```
**補足:**　python 3.5の環境で構築したい人は``pip2``を``pip3``に変更すればいいはず。

