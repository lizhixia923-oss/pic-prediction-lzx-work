---
title: "李之夏PIC数据预测模型"
collection: portfolio
type: "Machine Learning"
permalink: /portfolio/lzx-pic-prediction
date: 2026-01-17
excerpt: "构建李之夏PIC数据预测模型，用于相关数据的预测。"
header:
  teaser: /images/portfolio/lzx-pic-prediction/teaser.png
tags:
  - 数据预测
  - 机器学习
techstack:
  - name: Python
  - name: Scikit-learn
---

## 项目背景
项目旨在构建李之夏PIC数据预测模型，利用机器学习技术对PIC相关数据进行死亡风险预测。

## 核心实现
使用 Python + Scikit-learn 构建逻辑回归模型，并通过 SHAP 进行可解释性分析。

## 分析结果

![ROC曲线](/images/portfolio/lzx-pic-prediction/ROC-curve.png)
*图1 模型ROC曲线（AUC = 0.92）*

![混淆矩阵](/images/portfolio/lzx-pic-prediction/Confusion-Matrix.png)
*图2 测试集混淆矩阵*

![SHAP总结条形图](/images/portfolio/lzx-pic-prediction/shap-bar.png)
*图3 SHAP特征重要性摘要*

![SHAP蜂形图](/images/portfolio/lzx-pic-prediction/shap-bea.png)

![lab_5257_min依赖性图](/images/portfolio/lzx-pic-prediction/lab_5257_min.png)
