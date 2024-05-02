# Python_TradeBot
---
## Description
這是一個用 Python 實現的自動交易機器人

## Dependencies
```
pip install pandas
pip install talib #(要先在官網載到程式下)
pip install binance-futures-connector
pip install pyerror
```

## How to use
- Step.1 在程式中以下部分填入自己的金耀
```
from binance.um_futures import UMFutures 
import logging 
from binance.error import ClientError 
from binance.lib.utils import config_logging 
import pandas as pd 
import time 
from datetime import datetime 
import talib 
import csv 
#設定交易對
SYMBOL = 'ETHUSDT'

config_logging(logging, logging.DEBUG)
kline_data = pd.DataFrame()

#幣安API和API網址
API_KEY = '#your api key'
SECRET_KEY = 'your secret key'
BASE_URL = 'https://fapi.binance.com'

#Initialize the Binance client for futures trading
um_futures_client = UMFutures(key=API_KEY, secret=SECRET_KEY, base_url=BASE_URL)
```
- Step.2 直接執行:
```
python3.7 python_tradebot.py
```

## Demo
執行起來可見: https://youtu.be/sePS62w2-Mk
畫面中為執行範例，因為只是示範他執行起來長甚麼樣子所以並沒有放錢進到錢包去執行，最後面有出現一個 start time 那一行極為想要進行交易的時間點，但因為錢包沒有金錢所以終止下來

## 心得分享
Video link: https://youtu.be/LNYGguMOkfE
