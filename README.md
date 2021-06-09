# Geth Docker

使用Docker建立Geth私網環境  

## 環境

Geth使用port：8545  
Geth_Explorer使用port：8000

## 安裝

請在當前目錄下進行操作  

在終端機中執行：
`$ docker compose up`

或者在後台執行：
`$ docker compose up -d`

## 與Geth互動

在終端機中執行：
```
$ docker exec -it geth geth attach ipc:/geth_data/data/geth.ipc
```

## 區塊鏈資料說明

這個專案的做法為直接連上現成的私有鏈資料，不支援直接製作一個新的私有鏈。  
若想使用現成的私有鏈資料，請將專案中的`geth_data`資料夾的內容進行替換，請注意資料夾架構。