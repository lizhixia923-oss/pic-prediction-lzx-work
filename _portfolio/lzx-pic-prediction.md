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

![ROC曲线](/images/portfolio/lzx-pic-prediction/roc-curve.png)
*图1 模型ROC曲线（AUC = 0.92）*

![混淆矩阵](/images/portfolio/lzx-pic-prediction/confusion-matrix.png)
*图2 测试集混淆矩阵*

![SHAP全局重要性](/images/portfolio/lzx-pic-prediction/shap-summary.png)
*图3 SHAP特征重要性摘要*

模型在测试集上达到89.7 %灵敏度与94.0 %特异度，SHAP解释显示lab_5257_min为最具影响力指标。
