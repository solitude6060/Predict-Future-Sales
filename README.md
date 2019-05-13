# Predict-Future-Sales
## Project Description
Kaggle competition - Predict Future Sales for mid term in course DMAI  

## 開發語言及環境
- Python 3.6
- pandas for date analyzing and reading/writing
- sklearn for data preprocessing
- xgboost for regression tree model
- pickle for output data
- numpy
- itertools
---
- IDE : Jupyter Notebook

## 路徑及資料集 
1. 需創立input資料夾來放資料集
2. input資料夾中包含item.csv, shops.csv, categories.csv, sales_train_v2.csv, test.csv
3. output資料夾來存放處理完的資料和最終的submission.csv



## 資料前處理
1. 將資料的features的分佈畫出來後分析dataset
2. 可由1.得知data中有過於極端的值(ex:prize太高)或是沒有值(prize=0)以及重複資料的問題
3. 將以上資料去除或是改由平均數代替
4. 將處理好的資料輸出為pkl檔方便後續使用

## model
1. 嘗試以sklearn本身的linear regression來替代kernel範例中的，但資料特性較為發散所以效果不佳
2. 以多層dense加上linear的activate function，效果與上述差異不大
3. 嘗試將原kernel範例中的XGNRegressor的參數優化，多加了參數gamma，但效果更差
4. 多方嘗試後，還是先以原kernel的參數為主。

## 改良方向
1. 以時間序列性來看待整個資料，可以序列性模型例如RNN/LSTM來預測，但訓練時間會急速上升
2. 測試是否會有feature在模型中被視為噪音，不要加反而比較好
3. 使用params list的概念來測試最好的參數優化