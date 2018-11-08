# Coding
## STL lower_bound/upper_bound
对一个有序区间\[begin,end)执行二分查找，并返回目标位置,lower_bound查找第一个">="目标的位置，upper_bound查找第一个">"目标的
注意区间必须有序，且对象类型有"<"方法可以调用  
vector<int> vec = {1,2,3,4,4,5,6};//作用于vector，必须有序  
cout << lower_bound(vec.begin(), vec.end(), 4) - vec.begin() << endl;//3  
cout << upper_bound(vec.begin(), vec.end(), 4) - vec.begin() << endl;//5
## 快速幂 
