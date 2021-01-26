# 透過Jetson Nano 連接 intel Realsense D435i 進行目標偵測與測距

## 環境設定
### 安裝Tensorflow Lite Runtime套件程式
影像目標偵測採用SSD Mobilenet V2版本的Tensorflow Lite預訓練模型，因此必須要事先安裝Tensorflow Lite Runtime套件，安裝流程如下：
```bash
pip3 install https://github.com/google-coral/pycoral/releases/download/release-frogfish/tflite_runtime-2.5.0-cp36-cp36m-linux_aarch64.whl
```

### 安裝Realsense支援套件
#### Step1 安裝Swapfile提高JetsonNano記憶容量
目標:解決Jetson Nano內存壓力的問題，可以使用在USB的隨身碟或SSD上，預設擴充的內存為6GB。
```bash
git clone https://github.com/jetsonhacksnano/installSwapfile
cd installSwapfile
./installSwapfile.sh
```
