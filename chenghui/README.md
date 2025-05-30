# 基于随机森林和梯度提升树的乳腺癌检测与分析

本项目使用机器学习中的两种集成算法——随机森林（Random Forest）和梯度提升树（Gradient Boosting Decision Tree, GBDT）对乳腺癌数据进行建模、预测与分析。该分析旨在比较两种模型的性能，并通过数据可视化展示其分类效果，辅助医学诊断。

## 项目文件

* `基于随机森林和梯度提升树的乳腺癌检测与分析.ipynb`：Jupyter Notebook 主文件，包含数据预处理、建模、评估与可视化过程。
* `BCD_data.csv`：csv数据文件，包含jupyter中所用的数据集

## 使用的模型

* **随机森林（Random Forest）**

  * 多棵决策树的集成，使用投票进行分类。
* **梯度提升树（Gradient Boosting Decision Tree, GBDT）**

  * 基于梯度下降的提升方法，迭代地构建弱学习器。

## 数据集

* 数据来源：`sklearn.datasets.load_breast_cancer()`
* 样本数：569
* 特征数：30（例如：平均半径、平均纹理等）
* 标签：二分类（良性/恶性）

## 功能与流程

1. **数据加载与初步探索**

   * 使用 `pandas` 和 `seaborn` 进行数据可视化与特征分析
2. **特征缩放与划分数据集**

   * 使用 `StandardScaler` 进行归一化处理
   * 将数据划分为训练集和测试集
3. **模型训练**

   * 使用 `RandomForestClassifier` 和 `GradientBoostingClassifier` 分别进行训练
4. **性能评估**

   * 使用准确率（Accuracy）、混淆矩阵（Confusion Matrix）和 ROC 曲线进行评估
5. **结果可视化**

   * 使用 matplotlib 和 seaborn 绘制模型对比图与评估指标图

## 模型对比结果

| 模型 | Accuracy | Sensitivity | Specificity | Presision | F1-Score |
| ----- | ------ | ------ | ------ | ------ | ------ |
| GBDT | 95.6% | 93.0% | 97.2% | 95.2% | 96.2% |
| GBDT + PCA | 96.5% | 93.0% | 98.6% | 97.6% | 98.0% |
| GBDT + REF | 96.5% | 93.0% | 98.6% | 97.6% | 98.0% |
| RF | 95.6% | 93.0% | 97.2% | 95.2% | 96.2% |
| GBDT+PCA | 97.4% | 93.0% | 98.6% | 97.6% | 98.1% |
| GBDT+PCA | 96.7% | 93.0% | 97.2% | 95.2% | 96.2% |

## 使用方法

### 环境依赖

使用以下命令安装依赖环境：

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

### 运行步骤

```bash
jupyter notebook
```

打开 `基于随机森林和梯度提升树的乳腺癌检测与分析.ipynb` 文件，逐步运行每一个代码单元。

## 参考

* [Scikit-learn 官方文档](https://scikit-learn.org/)
* 乳腺癌数据集：[sklearn.datasets.load\_breast\_cancer](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)
