
# Minimind Learning
A personal practice on Minimind project
基於 MiniMind 輕量級大模型的本地訓練、微調與學習項目

> 原項目倉庫地址：[https://github.com/NekoNekodon/MinimindLearning/tree/main](https://github.com/jingyaogong/minimind)
> 定位：個人入門向大模型從零搭建、訓練調教、推理部署完整學習工程

## 項目簡介
本倉庫圍繞開源輕量級大模型 **MiniMind** 的學習鏈路，覆蓋從數據處理、模型初始化、預訓練、SFT監督微調、本地推理測試全流程。
本項目為個人學習項目，旨在吃透小參數大模型底層細節、不依賴封裝框架，純原生實踐 Transformer 架構訓練。

### 核心學習目標
1. 手動實現標準 Transformer Decoder 架構，理解注意力機制、RoPE 位置編碼、層歸一化、激活函數等底層細節；
2. 掌握語料清洗、構建自定義訓練數據集、批次封裝與 DataLoader 調優；
3. 完整跑通預訓練（Pre-train）+ 監督微調（SFT）兩階段訓練流程；
4. 本地 GPU 直接載入權重實現對話推理、溫度採樣、Top-p 採樣等解碼策略；
5. 配套調試工具：損失監控、梯度檢查、權重保存與繼續訓練斷點續訓。

## 技術棧
| 組件 | 用途 |
|------|------|
| PyTorch | 模型搭建、GPU 訓練、張量運算 |
| MiniMind | 基礎輕量 Decoder 大模型骨架 |
| transformers | 分詞器、基礎工具類 |
| numpy | 數據預處理、數值計算 |
| tqdm | 訓練進度可視化 |
| sentencepiece / huggingface tokenizer | 文本編解碼 |
