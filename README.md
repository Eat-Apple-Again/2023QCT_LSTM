### 使用LSTM來預測下個UE可能會註冊在哪個 Network SLice

## 說明

test_v2.ipynb -> 使用RNN或LSTM，劇本模擬UE移動性。
                 在這邊training和testing

data          -> 模擬的訓練資料(2023/10)，為期一個月，每30分鐘蒐集一次UE註冊的資訊

LSTM_model.png -> 用 torchviz印出LSTM的形狀

![image LSTM_structure](https://github.com/Eat-Apple-Again/2023QCT_LSTM/blob/main/LSTM_model.png?raw=true)


在test_v2.ipynb中選擇UE的訓練資料，資料前處理(imsi、tac、timestamp)做encoding

拆分成traning data和testing data

最後的輸出為透過LSTM預測下個UE可能註冊的tac(network slice)

這段code會部屬在QCT的server，我們在free5gc中加入NWDAF，驗證AnLF、MTLF的功能。