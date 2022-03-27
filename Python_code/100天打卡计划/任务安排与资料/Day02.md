# Day02



## 操作



|    步骤     |       操作       |
| :---------: | :--------------: |
| first step  | 数据预处理(回顾) |
| second step |    拟合训练集    |
| third step  |     预测结果     |
| fourth step |      可视化      |



## 解释



### First step

数据预处理与数据导入，只需要进行数据的导入以及数据集的划分(回顾)



### Second step

将训练集进行简单的线性拟合,训练一个线性模型



> CSDN博客：https://blog.csdn.net/lanhezhong/article/details/107768916
>
> 参考手册：https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html?highlight=linearregression#sklearn.linear_model.LinearRegression



### Third step

利用训练出的线性模型对测试集进行预测



> [CSDN博客](https://blog.csdn.net/weixin_45875105/article/details/107820838?ops_request_misc=&request_id=&biz_id=102&utm_term=sklearn%E9%AA%8C%E8%AF%81%E7%BA%BF%E6%80%A7%E6%A8%A1%E5%9E%8B%E5%A5%BD%E5%9D%8F&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-107820838.142^v5^pc_search_result_control_group,143^v6^register&spm=1018.2226.3001.4187)

### Fourth step

将训练集，测试集以及拟合曲线利用python包中的matplotlib包进行可视化

> [CSDN画图博客](https://yongqiang.blog.csdn.net/article/details/78608108?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_antiscanv2&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_antiscanv2&utm_relevant_index=1)