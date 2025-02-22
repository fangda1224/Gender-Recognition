性别预测工具

项目简介

本工具用于根据姓名预测不同地区的人的性别。通过机器学习模型，结合国家分类数据，能够对姓名进行性别预测，并输出预测结果及准确率。

功能

国家分类：根据国家将数据分组并保存为单独的CSV文件。

性别预测：使用逻辑回归模型对姓名进行性别预测。

结果整合：将预测结果整合到一个CSV文件中。

依赖库
pandas
numpy
scikit-learn
re
os
string

安装
克隆本仓库到本地：

bash

git clone https://github.com/yourusername/gender-prediction-tool.git

安装依赖库：

bash

pip install pandas numpy scikit-learn

使用说明

1. 数据准备
确保你的数据文件（如Excel或CSV）包含以下列：

corresponding author full：需要预测的姓名列。

last_reauthor_country：国家列。

2. 运行代码
国家分类：

代码会自动读取数据文件，并根据国家将数据分组保存到指定路径。

性别预测：

代码会读取训练数据和预测数据，训练模型并进行性别预测。

预测结果将保存到指定路径。

结果整合：

代码会将所有预测结果整合到一个CSV文件中。

3. 参数设置
confidence_level：设置预测的置信度阈值，默认为0.7。

train_path：训练数据路径。

file_path：预测数据路径。

out_path：预测结果保存路径。

4. 示例
python
# 设置参数
confidence_level = 0.7

train_path = 'path/to/train_data.csv'

file_path = 'path/to/prediction_data.csv'

out_path = 'path/to/output.csv'

# 运行预测
predict_gender(names)

文件结构
gender-prediction-tool/

├── README.md

├── gender_prediction.py

├── data/

│   ├── prediction_country_list.xlsx

│   ├── training_data/

│   └── prediction_results/

└── requirements.txt


许可证
本项目采用 MIT 许可证。详情请参阅 LICENSE 文件。

联系方式
如有任何问题，请联系 bobdurant1224@gmail.com。

注意：请确保在运行代码前，所有数据文件路径正确，并且依赖库已安装。
