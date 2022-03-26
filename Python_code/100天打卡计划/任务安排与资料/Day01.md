# Day01

![](/image/01.jpg)

## 操作

|    步骤     |            操作            |
| :---------: | :------------------------: |
| first step  | 导入numpy,pandas,sklearn库 |
| second step |         导入数据集         |
| third step  |        处理缺失数据        |
| fourth step |        编码分类数据        |
| fifth step  |     分开训练集与测试集     |
| sixth step  |          特征缩放          |





## 解释

### sklearn.preprocessing:Preprocessing and Normalization

> sklearn.preprocessing是对数据进行预处理和标准化的工具包



### first step

> 使用import导入包即可：numpy有各种数学函数用来处理数据，pandas用来导入数据集、管理数据集,sklearn中包含处理数据，机器学习分类处理模型等工具





---



### second step

> 使用pandas读取数据，将表格数据转化为矩阵与向量，方便处理





---



### third step

将缺失的数据使用平均值或中位数代替，这里使用sklearn中的Impute处理



> 参考资料：
>
> Impute(参考手册):https://scikit-learn.org/stable/modules/classes.html?highlight=impute#module-sklearn.impute
>
> 缺失值处理中fit,transform的作用：https://blog.csdn.net/weixin_38278334/article/details/82971752
>
> 缺失值多变量填充：https://blog.csdn.net/weixin_43569478/article/details/112914795



---



### fourth ste

分类数据(定性数据)与定量数据相对，指的是性别，地区，评分等级等，无法作为数值进行处理，需要将他们转化为数值(如男：0，女：1)，使用sklearn.preprocessing里的LabelEncoder即可

假如有三种颜色特征：红、黄、蓝。 在利用机器学习的算法时一般需要进行向量化或者数字化。那么你可能想令 红=1，黄=2，蓝=3. 那么这样其实实现了标签编码，即给不同类别以标签。然而这意味着机器可能会学习到“红<黄<蓝”，但这并不是我们的让机器学习的本意，只是想让机器区分它们，并无大小比较之意。所以这时标签编码是不够的，需要进一步转换。因为有三种颜色状态，所以就有3个比特。即红色：1 0 0 ，黄色: 0 1 0，蓝色：0 0 1 。如此一来每两个向量之间的距离都是根号2，在向量空间距离都相等，所以这样不会出现偏序性，基本不会影响基于向量空间度量算法的效果。



> 分类数据转化的意义以及LabelEnconder与HotEnconder的作用区别：[CSDN博客](https://blog.csdn.net/accumulate_zhang/article/details/78510571?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164827123716780357289243%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=164827123716780357289243&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-4-78510571.142^v5^pc_search_result_control_group,143^v6^register&utm_term=OneHotEncoder&spm=1018.2226.3001.4187)
>
> [博客](https://blog.csdn.net/qq_39072627/article/details/120740720?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_antiscanv2&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_antiscanv2&utm_relevant_index=1)
>
> 参考手册：https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelEncoder.html?highlight=labelencoder#sklearn.preprocessing.LabelEncoder
>
> [onehotencoder更新](https://stackoverflow.com/questions/54345667/onehotencoder-categorical-features-deprecated-how-to-transform-specific-column)



---



### fifth step

划分训练集与测试集，使用sklearn中sklearn.crossvalidation中的train_test_split()来进行划分



> [CSDN博客](https://blog.csdn.net/wade1203/article/details/91453804?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164827349216780274153863%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=164827349216780274153863&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-1-91453804.142^v5^pc_search_result_control_group,143^v6^register&utm_term=sklearn%E5%88%92%E5%88%86%E6%B5%8B%E8%AF%95%E9%9B%86%E4%B8%8E%E8%AE%AD%E7%BB%83%E9%9B%86&spm=1018.2226.3001.4187)





---



### sixth step

特征值：样本在某个特征属性上的取值，如花朵数据集中，花朵的花茎长度为7.5

特征值缩放的作用：在机器学习中，我们会使用特征向量之间的欧氏距离计算，如果不同的特征值的取值范围不同(花茎长短为1-10,甜度为0-100)，取值范围大的对学习模型影响更大，为了减少取值范围不同     带来的误差，进行特征标准化统一范围

可以使用sklearn.preprocessing中的StandardScalar进行标准化

> 参考手册：https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html?highlight=standardscaler#sklearn.preprocessing.StandardScaler



---









> 参考网站：
>
> git项目英文地址：https://github.com/Avik-Jain/100-Days-Of-ML-Code
>
> sklearn参考文档：https://scikit-learn.org/stable/



