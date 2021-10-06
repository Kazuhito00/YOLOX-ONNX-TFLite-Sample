# YOLOX-ONNX-TFLite-Sample
[YOLOX](https://github.com/Megvii-BaseDetection/YOLOX)のPythonでのONNX、TensorFlow-Lite推論サンプルです。<br>
ONNX、TensorFlow-Liteに変換したモデルも同梱しています。変換自体を試したい方は[YOLOX_PyTorch2TensorFlowLite.ipynb](YOLOX_PyTorch2TensorFlowLite.ipynb)を使用ください。<br>

https://user-images.githubusercontent.com/37477845/136243868-7a6437ae-47ba-4696-aa03-f83e051bb8bc.mp4

# Requirement 
* Pytorch 1.9.0 or later
* apex 0.1 or later
* pycocotools 2.0 or later
* OpenCV 3.4.2 or later
* onnxruntime 1.5.2 or later

# Demo
デモの実行方法は以下です。
```bash
python sample_onnx.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --image<br>
画像ファイルの指定 ※指定時はカメラデバイスや動画より優先<br>
デフォルト：指定なし
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：960
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：540
* --model<br>
ロードするモデルの格納パス<br>
デフォルト：model/yolox_nano.onnx
* --input_shape<br>
モデルの入力サイズ<br>
デフォルト：416,416
* --score_th<br>
クラス判別の閾値<br>
デフォルト：0.3
* --nms_th<br>
NMSの閾値<br>
デフォルト：0.45
* --nms_score_th<br>
NMSのスコア閾値<br>
デフォルト：0.1
* --with_p6<br>
Large P6モデルを使用するか否か<br>
デフォルト：指定なし

```bash
python sample_tlite.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --image<br>
画像ファイルの指定 ※指定時はカメラデバイスや動画より優先<br>
デフォルト：指定なし
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：960
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：540
* --model<br>
ロードするモデルの格納パス<br>
デフォルト：model/yolox_nano_float16_quantize.tflite
* --input_shape<br>
モデルの入力サイズ<br>
デフォルト：416,416
* --score_th<br>
クラス判別の閾値<br>
デフォルト：0.3
* --nms_th<br>
NMSの閾値<br>
デフォルト：0.45
* --nms_score_th<br>
NMSのスコア閾値<br>
デフォルト：0.1
* --with_p6<br>
Large P6モデルを使用するか否か<br>
デフォルト：指定なし

# Reference
* [Megvii-BaseDetection/YOLOX](https://github.com/Megvii-BaseDetection/YOLOX)

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
YOLOX-ONNX-TFLite-Sample is under [Apache-2.0 License](LICENSE).

# License(Movie)
サンプル動画は[NHKクリエイティブ・ライブラリー](https://www.nhk.or.jp/archives/creative/)の[イギリス ウースターのエルガー像](https://www2.nhk.or.jp/archives/creative/material/view.cgi?m=D0002011239_00000)を使用しています。
