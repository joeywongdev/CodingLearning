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
求a的b次幂 ： a^b  
  以a^11为例，正常需要a乘11次，即复杂度O(n)  
  可以分解为求a^(2^3 + 2^0 + 2^1 + 2^1) = a^8 * a^2 * a^1  
  计算的过程为：a * a，保存临时结果a2，然后计算a2 * a2作为a4，然后计算a4 * a4作为a8，最后计算 a * a2 * a8  
  大大减少了计算次数  
  实际编码的时候注意使用long long int，防止溢出  
