# datascience检索表

---

from datascience import *
import pandas as pd
data1=pd.read_csv("hadoop.csv")
data2=pd.read_csv("hive.csv")
data3=pd.read_csv("spark.csv")
data4=pd.read_csv("高数监考表.csv")
datas=pd.concat([data1,data2,data3,data4],ignore_index=True )
datas.to_csv("sc.csv")
s= Table.read_table("sc.csv")
t=s.where("学号",are.equal_to("赵晓柔"))
print(t)

结果：
 E:/soft/python3_11/Project/cloud01.py
Unnamed: 0 | 姓名          | 学号   | 日期         | 时间          | 教室    | 科目
15         | 2.02015e+09 | 赵晓柔  | 2022/11/15 | 14:30-16:30 | 教一404 | hive

Process finished with exit code 0



