# Day03



## 操作

|    步骤     |              操作              |
| :---------: | :----------------------------: |
| first step  |   导入numpy,pandas,sklearn库   |
| second step |           导入数据集           |
| third step  | 编码分类数据(避免虚拟变量陷阱) |
| fourth step |       分开训练集与测试集       |
| fifth step  |       训练模型，预测结果       |







## 资料







### Third Step

编码分类数据(避免虚拟变量陷阱),这里的虚拟变量陷阱指的是：如性别中，我们使用[0,1]代表男，[1,0]代表女，其中$x_1=1代表女性，x_1=0代表男性，也就是说，x_1+x_2恒等于1，x_1与x_2可以互相表示，满足线性关系$  

根据高等代数的知识我们可以知道，在上述情况下，矩阵 X 是不满秩的，因此不存在 $X^{-1}$ ，导致最小二乘法不能估计参数。

因此，我们只需要[0]表示男性，[1]表示女性来消除这种多重共线性。

`注意：`虽然我们使用LabelEncoder直接进行编码得到的结果相同，也是0代表男性，1代表女性，但意义是完全不同的

> 更详细的解释可以参考这些资料：
>
> [虚拟变量陷阱](https://blog.csdn.net/weixin_30732825/article/details/101073777?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164846891016780357275668%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=164846891016780357275668&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-1-101073777.142^v5^pc_search_result_control_group,143^v6^register&utm_term=%E8%99%9A%E6%8B%9F%E5%8F%98%E9%87%8F%E9%99%B7%E9%98%B1%E6%98%AF%E4%BB%80%E4%B9%88&spm=1018.2226.3001.4187)
>
> [多重共线性](https://blog.csdn.net/Clifnich/article/details/53758585?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522164846932716780271570164%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=164846932716780271570164&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-1-53758585.142^v5^pc_search_result_control_group,143^v6^register&utm_term=%E5%8F%98%E9%87%8F%E9%97%B4%E5%87%BA%E7%8E%B0%E5%AE%8C%E5%85%A8%E5%85%B1%E7%BA%BF%E6%80%A7&spm=1018.2226.3001.4187)







其他的步骤操作见代码与之前的解释