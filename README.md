### 使用LSTM來預測下個UE可能會註冊在哪個 Network Slice

## 說明

在 test_v2.ipynb 中選擇UE的訓練資料，資料前處理(imsi、tac、timestamp)做 encoding  
拆分成 traning 和 testing data  
最後的輸出為透過 LSTM 預測下個 UE 可能註冊的 tac(network slice)  
這段 code 會部屬在 QCT 的 server，我們在 free5gc 中加入 NWDAF，驗證 AnLF、MTLF 的功能。  

****

test_v2.ipynb -> 使用 RNN 或 LSTM，劇本模擬UE移動性。
                 在這邊 training 和 testing

data          -> 模擬的訓練資料(2023/10)，為期一個月，每30分鐘蒐集一次UE註冊的資訊

LSTM_model.png -> 用 torchviz 印出 LSTM 的形狀

![image LSTM_structure](https://github.com/Eat-Apple-Again/2023QCT_LSTM/blob/main/LSTM_model.png?raw=true)