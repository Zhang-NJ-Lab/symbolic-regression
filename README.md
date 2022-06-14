# symbolic-regression
0107.xlsx  原始数据集（表格，含有输入特征和输出数据）
Code.py 主代码(前半部分是传统SR， 后半部分t-SR)


t-SR时皮尔森系数从0.39升到-0.43(目前只计算了皮尔森系数r；MSE, RMSE; MAE, R2等其他准确率评判数据需要进一步生成，目前还未计算）：

原始SR输出（默认）：
超参数为：population_size=1000,      generations=91, stopping_criteria=0.01,
                           p_crossover=0.8, p_subtree_mutation=0.05,
                           p_hoist_mutation=0.05, p_point_mutation=0.05,
                           max_samples=0.9, verbose=1,
                           parsimony_coefficient=0.01, random_state=None,n_components=100)
需注意随机生成operator和特征变量组合，所以同样超参数每次运行结果不同
                           
                           
[mul(mul(X6, X3), X1),
 sub(X20, mul(X6, X1)),
 sub(div(add(mul(X21, X5), sub(X22, X21)), div(add(X20, X15), add(X7, X12))), div(mul(sub(X8, -0.626), div(X18, X17)), mul(sub(X18, X2), add(X6, X22)))),
 mul(X6, X1),
 mul(X3, X1),
 mul(add(mul(add(X15, X4), sub(X18, X16)), add(mul(X1, X0), mul(X18, X21))), mul(mul(add(X2, X21), div(X9, X13)), add(sub(X6, X10), add(X18, X11)))),
 mul(X1, div(X6, X18)),
 add(X3, X1),
 add(sub(X14, X20), add(X2, X1)),
 add(X5, mul(X3, X1)),
 div(mul(X21, X1), add(mul(X19, X15), mul(X10, X16))),
 div(sub(X3, X20), mul(X4, X8)),
 add(X8, X10),
 div(X7, X8),
 sub(X20, X1),
 div(X1, X8),
 div(X3, mul(div(X0, X3), X4)),
 add(X1, X1),
 div(sub(add(sub(add(X21, X3), sub(X9, X22)), add(sub(X12, X10), add(X13, X4))), sub(div(div(X9, X8), add(X19, X6)), div(div(X6, X3), mul(-0.136, X16)))), mul(sub(add(mul(X1, X11), add(X19, X20)), add(div(-0.332, X17), sub(X15, X20))), add(sub(add(X8, X15), sub(X5, X13)), sub(div(X2, X16), mul(X18, 0.892))))),
 sub(X3, X20),
 mul(mul(mul(X12, X3), mul(X5, X21)), div(mul(X8, X6), mul(X18, X4))),
 mul(X5, X21),
 sub(X5, X10),
 div(X1, mul(X9, X14)),
 sub(X10, X1),
 div(add(X3, X15), add(X12, X19)),
 add(sub(X20, X2), X16),
 div(X1, X14),
 sub(div(X1, X7), sub(X12, X1)),
 div(X2, X15),
 add(X3, X6),
 div(-0.149, X10),
 mul(add(X21, X16), X3),
 mul(div(add(X19, X2), add(-0.622, X1)), mul(add(X4, X15), div(X15, X7))),
 mul(X8, X10),
 add(mul(sub(X2, 0.973), X18), X2),
 mul(add(div(X8, X15), sub(X18, X4)), div(add(X8, X20), mul(X3, X8))),
 mul(mul(sub(X11, X0), sub(X4, X20)), mul(add(X1, X22), add(X8, X19))),
 add(add(add(X17, X1), sub(X3, X16)), add(sub(X9, X17), mul(X0, X1))),
 mul(add(X4, X14), X2),
 add(div(mul(mul(add(mul(X1, X16), div(X11, X8)), add(sub(X17, X21), sub(X21, X0))), mul(add(mul(X16, X0), add(X8, X0)), mul(mul(X10, X19), mul(X21, X6)))), mul(div(mul(sub(X15, X21), add(X18, X18)), div(mul(X13, X8), add(X15, X4))), mul(add(mul(X15, X10), add(X17, X20)), sub(add(X17, X3), sub(X3, X0))))), mul(mul(div(div(mul(X1, X9), sub(X9, X19)), div(div(X14, X6), mul(X17, X3))), div(sub(add(X15, X17), sub(X11, X6)), div(sub(X12, X6), sub(X10, X13)))), mul(div(add(sub(X4, X10), sub(X1, X2)), div(add(X12, X1), div(X4, X15))), div(add(div(X8, X10), mul(X2, X21)), sub(add(X2, X12), sub(X8, X11)))))),
 add(sub(X3, X20), X9),
 add(sub(sub(mul(X5, X17), mul(X21, X17)), mul(sub(X17, X10), mul(X19, X17))), sub(sub(add(X10, X2), add(X13, X22)), add(div(X15, X2), div(X7, X1)))),
 add(div(add(sub(div(0.444, X13), div(X5, X19)), sub(div(X20, X22), mul(X22, X3))), div(div(add(X22, X2), mul(X19, X7)), sub(add(X18, X10), mul(-0.583, X14)))), div(sub(sub(add(X17, X17), sub(X13, X5)), mul(div(X0, X0), sub(X14, 0.843))), div(sub(add(X20, X17), sub(X11, X12)), mul(sub(X12, X5), div(X3, X10))))),
 mul(sub(add(div(X20, X2), div(X1, -0.743)), sub(add(X7, X19), mul(X16, X2))), mul(mul(div(X6, X19), sub(X13, X1)), add(mul(X20, X0), div(X9, X9)))),
 div(0.093, X1),
 mul(X3, X3),
 add(X1, X5),
 div(X10, X2),
 sub(X4, X3),
 add(X2, -0.016),
 sub(X17, sub(X1, mul(sub(X5, mul(X1, X8)), X4))),
 add(X18, sub(X0, X19)),
 add(X21, X0),
 sub(mul(sub(X8, X0), add(X17, X1)), add(mul(X5, X14), add(X1, X9))),
 add(sub(X4, X3), X19),
 add(X3, X0),
 div(add(sub(mul(add(sub(X18, X15), add(X15, X17)), add(div(X12, X18), div(X21, X6))), sub(sub(div(0.471, X10), div(X3, X8)), div(add(X15, X12), add(X9, X12)))), add(add(mul(div(X17, X20), sub(X22, X16)), sub(mul(X1, X1), div(X5, X20))), div(mul(mul(X19, X1), add(X6, X15)), mul(div(X9, X15), add(X20, X21))))), add(sub(add(div(div(X15, X2), add(X9, X9)), div(add(X0, X1), sub(X21, X8))), mul(sub(div(X17, X15), div(X0, X16)), sub(sub(X20, X18), mul(X12, X1)))), sub(mul(mul(add(X7, X10), div(X4, X6)), mul(mul(X0, X3), div(X3, X13))), mul(add(div(X9, X6), add(X0, X12)), div(add(X6, X13), mul(X8, X0)))))),
 div(mul(X10, X20), X1),
 div(X13, mul(X7, mul(X16, X10))),
 mul(0.076, X3),
 mul(X20, X19),
 mul(X18, X2),
 mul(add(X1, 0.211), add(X8, X7)),
 div(X12, X2),
 add(add(mul(X2, X11), add(X7, X2)), add(div(X1, X2), div(X2, X18))),
 sub(mul(mul(sub(X3, X3), mul(X6, X11)), mul(mul(X7, X15), mul(X18, X1))), sub(mul(add(X18, X7), sub(X13, X20)), sub(sub(X20, X2), mul(X1, X15)))),
 div(sub(div(X18, X0), X2), X5),
 sub(add(X1, X14), X20),
 mul(X2, X7),
 sub(X11, X1),
 mul(X2, add(X4, X18)),
 mul(mul(mul(X6, X2), div(X5, X2)), sub(mul(X5, X4), div(X22, X14))),
 add(add(mul(mul(X3, X20), div(X12, X18)), sub(mul(X12, X21), add(X20, X10))), mul(mul(mul(X22, X18), mul(X13, X2)), sub(mul(X19, X7), add(X6, X0)))),
 div(X2, mul(X14, mul(X18, X7))),
 div(sub(sub(mul(mul(X17, X22), sub(X7, X13)), sub(sub(X20, X20), add(X13, X22))), div(add(sub(X4, X2), add(X5, X18)), sub(mul(X15, X2), div(X18, X14)))), sub(sub(mul(add(X11, X9), mul(X3, X16)), add(add(X5, X13), div(X22, X18))), add(sub(mul(X3, X15), sub(X14, X6)), add(mul(X5, X22), div(X2, X20))))),
 add(X6, X7),
 div(X12, X2),
 add(sub(X1, X6), mul(X7, X6)),
 add(add(X22, X0), div(X3, X19)),
 mul(add(div(sub(div(X8, X0), mul(X11, X17)), div(sub(X7, X9), div(X20, X0))), mul(mul(add(X4, X10), div(X0, X8)), sub(add(X14, X12), div(X2, X9)))), div(mul(add(div(X20, X10), sub(X16, X11)), add(div(X19, -0.387), div(X9, X15))), sub(add(add(X20, X15), sub(X21, X7)), sub(add(X4, X19), div(X2, X9))))),
 div(X21, 0.829),
 add(mul(add(X14, X19), mul(X5, X3)), mul(sub(X22, X12), sub(X9, X9))),
 sub(X1, X7),
 add(add(div(sub(mul(X18, X8), div(X15, X15)), sub(mul(-0.391, X5), sub(X9, X7))), add(mul(mul(X11, X2), sub(X1, X22)), mul(add(X12, X13), div(X11, -0.512)))), sub(mul(mul(sub(X2, X4), sub(X15, X18)), mul(sub(X13, X22), add(X22, X5))), add(sub(sub(X0, X11), sub(X3, X9)), div(sub(X22, X5), div(X15, X2))))),
 div(X10, add(0.422, X1)),
 mul(div(X3, X7), add(X0, 0.608)),
 sub(X15, X3),
 sub(X12, X1),
 sub(sub(sub(mul(X19, X0), add(X5, X14)), mul(div(-0.749, X0), mul(X22, X14))), add(add(mul(X9, X3), sub(X3, X5)), sub(sub(X21, X10), add(X4, X7)))),
 mul(X0, X7),
 add(div(sub(div(X15, X16), sub(X4, X13)), sub(sub(X8, X7), div(X22, X1))), div(sub(div(X8, X22), mul(X2, X22)), div(sub(X1, X3), mul(X4, X18)))),
 add(mul(div(add(X11, X6), div(X17, X2)), mul(div(X12, X12), sub(X2, X19))), add(add(add(X3, X19), add(X15, X6)), mul(sub(X10, X10), mul(X1, 0.096)))),
 mul(X1, X15),
 add(mul(X18, X7), X2),
 add(0.295, mul(X2, X16)),
 add(add(mul(X15, X20), sub(X7, X21)), div(mul(X11, X8), div(X2, X20))),
 div(add(X18, X12), mul(X19, X10)),
 add(X13, X1),
 add(mul(X15, X19), sub(X3, X10))]
0.3672278454925347 1
0.35088016639654024 12
0.3467226914805537 14
0.3219213897483089 34



**t-sr输出**
D:\NLP-Examples\pythonProject1\venv\Scripts\python.exe D:/NLP-Examples/pythonProject1/SR/Code.py
    |   Population Average    |             Best Individual              |
---- ------------------------- ------------------------------------------ ----------
 Gen   Length          Fitness   Length          Fitness      OOB Fitness  Time Left
   0    26.05          0.10791       31         0.402845         0.118691      1.07m
0.3947151468614388 3
0.3750015365554344 5
0.35088016639654024 6
0.3490623132075035 13
0.36038298010415276 14
0.35088016639654024 16
0.3600302918282939 17
0.35088016639654024 19
0.3526158317185049 20
0.32625950687967775 22
0.33565840128865976 26
0.32495365683555943 27
0.3219575113611538 29
D:\NLP-Examples\pythonProject1\venv\lib\site-packages\numpy\lib\function_base.py:2829: RuntimeWarning: invalid value encountered in true_divide
  c /= stddev[:, None]
D:\NLP-Examples\pythonProject1\venv\lib\site-packages\numpy\lib\function_base.py:2830: RuntimeWarning: invalid value encountered in true_divide
  c /= stddev[None, :]
**-0.4323155223757824**
1 13 4 13
0.4323155223757824
1 13 13 4
-0.4323155223757824
4 13 1 13
0.4323155223757824
4 13 13 1
0.4323155223757824
13 1 4 13
-0.4323155223757824
13 1 13 4
0.4323155223757824
13 4 1 13
-0.4323155223757824
13 4 13 1

Process finished with exit code 0
