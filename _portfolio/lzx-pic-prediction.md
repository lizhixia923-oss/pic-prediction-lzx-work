---
title: "李之夏 PIC 数据预测模型"
collection: portfolio
type: "Machine Learning"
permalink: /portfolio/lzx-pic-prediction
date: 2026-01-17
excerpt: "基于机器学习方法构建 PIC 数据预测模型，并结合 SHAP 方法对模型结果进行可解释性分析。"
header:
  teaser: /images/portfolio/lzx-pic-prediction/Confusion_Matrix.png
tags:
  - 数据预测
  - 机器学习
  - 可解释性分析
techstack:
  - name: Python
  - name: Scikit-learn
  - name: SHAP
---

## 项目背景（Background）

PIC（Post Intensive Care / Pediatric Intensive Care）相关数据通常具有变量维度高、非线性关系复杂等特点，传统统计方法在预测性能和解释能力方面均存在一定局限。本项目基于 PIC 相关临床与实验室数据，构建机器学习预测模型，用于对目标结局进行预测，并探索关键影响因素。

在模型构建完成后，引入 SHAP（SHapley Additive exPlanations）方法，对模型预测结果进行可解释性分析，以增强模型在医学与临床研究场景中的可理解性和可信度。

---

## 核心实现（Implementation）

本项目以 Python 为主要开发语言，使用 Scikit-learn 构建预测模型。主要流程包括：

1. **数据预处理**：对原始 PIC 数据进行清洗、缺失值处理及特征筛选；
2. **模型训练**：基于多维实验室指标及人口学变量训练预测模型；
3. **模型评估**：通过交叉验证与性能指标评估模型预测能力；
4. **可解释性分析**：使用 SHAP 方法量化各特征对模型输出的贡献，并分析其作用方向。

---

## 分析结果（Results & Analysis）

### 特征重要性分析

下图展示了基于 SHAP 值的特征重要性排序结果，横轴为各特征对模型预测影响的平均绝对 SHAP 值。

![SHAP Feature Importance](/images/portfolio/lzx-pic-prediction/SHAP_bar.png)

结果显示，**lab_5257_min** 对模型预测的贡献最大，是最关键的预测变量；**lab_5225_range、lab_5235_max 及 lab_5227_min** 也表现出较高的重要性，而 **age_month** 在模型中的整体影响较小。

---

### 特征取值与预测方向关系

下图为 SHAP 总结散点图（beeswarm plot），展示了各特征取值大小及其对模型预测结果的方向性影响。

![SHAP Summary Plot](/images/portfolio/lzx-pic-prediction/shap_bea.png)

可以观察到，不同实验室指标在取值升高或降低时，对模型预测结果具有明显的正向或负向影响，提示这些变量在预测结局中可能具有重要的临床或生物学意义。

---

## 总结（Conclusion）

本项目成功构建了 PIC 数据预测模型，并通过 SHAP 方法实现了模型结果的可解释性分析。结果表明，多个实验室指标在模型预测中起主导作用，而人口学变量的影响相对有限。该研究为 PIC 相关数据的预测分析与解释提供了一种可行的技术路径。
