# cpp-cp-template

This is a template for compettive programming in c++. It has tried to implemented a iterator type in c++ just like in rust.
Here is an example:
```c++
#include "cpp_template.cpp"
int main()
{
  fast_io();
  cout<<"auto xc = range(7);\nVec<int> z = xc.map_to<int>([](auto x) { return x * 2; }).collect();\ncout<<z;";
  auto xc = range(7);
   Vec<int> z = xc.map_to<int>([](auto x) { return x * 2; }).collect();
    cout<<z;
   cout << "range(10).tuple_with(range(5)):";
   range(10).tuple_with<int>(range(5)).debug_print();
   cout << "rangeproductiter([4,2]):";
   range_product_iter<2>({4, 5}).debug_print();
   cout << " Vec<i32> x{1, 2, 3, 4, 5, 5, 6, 7};\ntupleiter(range(x.size()).collection_iter(x.data()),range(1, x.size()).collection_iter(x.data())).debug_print();";
   Vec<i32> x{1, 2, 3, 4, 5, 5, 6, 7};
   tupleiter(range(x.size()).collection_iter(x.data()),range(1, x.size()).collection_iter(x.data())).debug_print();
    cout << "range(20).enumarate:";
    range(20).enumarate().debug_print();
    cout << "for(auto x:range(20).rev()){cout<<x<<\" \";}\n";
    for (auto x : range(20).rev()) {
      cout << x << " ";
    }
}
```
The output of this code is:
```
auto xc = range(7);
Vec<int> z = xc.map_to<int>([](auto x) { return x * 2; }).collect();
cout<<z;[0,2,4,6,8,10,12,]
range(10).tuple_with(range(5)):[(0, 0),(1, 1),(2, 2),(3, 3),(4, 4),]
rangeproductiter([4,2]):[[0,0,],[1,0,],[2,0,],[3,0,],[0,1,],[1,1,],[2,1,],[3,1,],[0,2,],[1,2,],[2,2,],[3,2,],[0
,3,],[1,3,],[2,3,],[3,3,],[0,4,],[1,4,],[2,4,],[3,4,],]
 Vec<i32> x{1, 2, 3, 4, 5, 5, 6, 7};
tupleiter(range(x.size()).collection_iter(x.data()),range(1, x.size()).collection_iter(x.data())).debug_print()
;[(1, 2),(2, 3),(3, 4),(4, 5),(5, 5),(5, 6),(6, 7),]
range(20).enumarate:[(0, 0),(1, 1),(2, 2),(3, 3),(4, 4),(5, 5),(6, 6),(7, 7),(8, 8),(9, 9),(10, 10),(11, 11),(1
2, 12),(13, 13),(14, 14),(15, 15),(16, 16),(17, 17),(18, 18),(19, 19),]
for(auto x:range(20).rev()){cout<<x<<" ";}
19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 0 

```
