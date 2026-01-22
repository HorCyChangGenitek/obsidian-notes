# 麥克風降噪


由於，台灣的天氣使的我們經常會使用電扇，但這些電扇的噪音常會使得麥克風的收音品質變很差。
最近發現了將電腦固定式麥克風 或是web內建麥克風，做到基礎降噪。


## 下載
Equalizer APO[https://equalizerapo.com/]
RnNoise [https://github.com/werman/noise-suppression-for-voice]

## 安裝及解壓縮
安裝Equalizer APO，並且將RNNoise解壓縮到APO的插件Folder。
```
C:\Program Files\EqualizerAPO\VSTPlugins
```

## 設定
開啟APO開始設定，
請記住 預設的config.txt是APO一定會執行的路徑，
我們應該要開一個新的profile如`mic.txt` 並且將config.txt指一個`include:mic.txt`
![](files/Pasted%20image%2020241018150713.png)

接著可以開始設定我們的`mic.txt`
先使用selected devices指定我們的麥克風，接著插入VST plugin 找到你的 dll
像我這樣`win-rnnoise\vst\rnnoise_stereo.dll`
(stereo與mono差別在於立體音軌與單音軌)
插入完畢你可以open panel來設定，也可以 option->embed
![](files/Pasted%20image%2020241018151420.png)

## 如果
如果你的固定式麥克風聲音小到很難聽的清楚，可以先在Windows的音效管理員設定將db加到滿，這樣透過APO與RNNoise就可以降噪，也可以在音效管理員那邊看到有沒有爆音等資訊。
如果還是太小聲，建議再降噪以後再用`Preamp`放大聲音，這樣才不容易在音量大的時候糊掉，
放大以後建議設定一個`Peaking filter`可以降低你的最大音量到指定db (我是指定-6db)



![](files/Pasted%20image%2020241018150822.png)




