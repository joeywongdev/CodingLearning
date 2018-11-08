# Coding
## 1. STL lower_bound/upper_bound
对一个有序区间\[begin,end)执行二分查找，并返回目标位置,lower_bound查找第一个">="目标的位置，upper_bound查找第一个">"目标的
注意区间必须有序，且对象类型有"<"方法可以调用  
vector<int> vec = {1,2,3,4,4,5,6};//作用于vector，必须有序  
cout << lower_bound(vec.begin(), vec.end(), 4) - vec.begin() << endl;//3  
cout << upper_bound(vec.begin(), vec.end(), 4) - vec.begin() << endl;//5  
map<int, string> mm;//由于stl map内部的红黑树的特性，天然具有二分查找的特性，所以stl为map提供了专门的方法
mm.insert(std::make_pair(1,"a"));  
mm.insert(std::make_pair(2,"b"));  
mm.insert(std::make_pair(3,"c"));  
mm.insert(std::make_pair(4,"d"));  
mm.insert(std::make_pair(5,"e"));  
cout << "3 lower_bound -> " << mm.lower_bound(3)->second << endl;  
cout << "3 upper_bound -> " << mm.upper_bound(3)->second << endl;
## 2. 快速幂 
