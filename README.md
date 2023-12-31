# RemoteAudioSwitcher
## 製作動機
- 因為平常有躺在床上聽音樂的習慣，但是又懶得從床上爬起來去調整喇吧音量，又或者是有時候想睡覺，電腦音量忘記關訊息提示，此時我就想手機都在身上，能否用手機來控制電腦音效卡輸出以及音量，然後此專案就誕生了...
- 因為目前在當兵沒什麼時間，這個成品利用假日從0到1，只花了1天的時間，所以代碼非常的亂之後有空再整理@@

## 電腦所需環境
- python3.0
- netFramework 4.7.2

## 原理
- 利用Windows api去獲取本機的音效卡，以及控制本機的音量。
- 然後利用JsonRPC的方式通訊，c#端為Server，python端為Client。
- python端實現WebAPI以及簡易的Flask Web，在板模中利用Jquery js來做Web api callback，python收到callback後再去呼叫jsonRpc下指令給c# Server端。

## Python所需套件
- 首先你的電腦要有Python3，然後打開你電腦的cmd，把下面的指令貼上，即可自動安裝。
```shell
pip install json-rpc
pip install Flask
pip install Flask-Cors
```

## 使用方法
1. 下載Release檔案，[點我跳轉](https://github.com/godchadigo/RemoteAudioSwicher/releases/tag/new)
2. 解壓縮檔案後，雙擊start.bat
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/db797746-af22-4d5d-9a24-94c9fdba2426)
4. 訪問http://yourIP:5000/device  (yourIP再啟動start.bat時會顯示)
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/f8e4b9ae-c9cd-4b38-bd5a-5f47c99f4f41)
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/c3ea8227-2c7f-435c-89ac-7778ad7d9cca)


## 作品分享
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/2c9c4ab0-a8e2-497a-af84-e81606eba4bc)
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/82544e6c-05c8-4625-bae4-7f76294d12f8)
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/13c80b65-2708-4f7d-ade4-42bd8a700108)
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/e7dc7fe9-0ff8-424e-b2c7-1ae14d3869b9)
![image](https://github.com/godchadigo/RemoteAudioSwicher/assets/19208239/54dbe1f5-8e77-4978-947d-ab4376bad5b1)

## 借助工具
[AudioSwitcher](https://github.com/xenolightning/AudioSwitcher)
[Touchsocket](https://github.com/RRQM/TouchSocket)
[json-rpc1.15.0](https://pypi.org/project/json-rpc/)
[Flask](https://pypi.org/project/json-rpc/)
