# 04_imu_tk_assignment #

1.创造MultiPosAccCostFunction类，继承自SizedCostFunction，其中residual为常数，parameter为(S_xz，S_xy，S_yx，K1，K2，K3，b_x，b_y，b_z)共九个，因此SizedCostFunction大小为<1，9>


2.类构造函数输入为g值和观测值


3.Ealuation函数内，首先一下三角形式构建calib_triad，将观测值保存为Eigen矩阵形式raw_samp，同时计算得到预测值calib_samp，residual以课件中的形式给出，jacobians矩阵由计算得到，计算过程在作业附件中。(计算过程中的安装误差矩阵与代码的写法保持一致，不同于课件里的命名)


4.初始化parameter的时候选择相应位置的安装误差值进行赋值
