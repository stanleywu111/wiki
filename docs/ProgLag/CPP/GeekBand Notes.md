# 参数传递与返回值
* 尽量使用引用传递参数
* 如果参数没有被改变，则加const
* 相同class的各个object互为友元
* 函数体内返回local对象，则函数不可以返回引用，因为函数结束的时候local对象已经释放掉，引用无法找到该local对象。

```cpp
void func1(Cls* probj) { prob->xxx(); }
void func2(Cls obj)    { obj.xxx();   }
void func3(Cls& obj)   { obj.xxx();   }

Cls obj;

func1(&obj);
func2(obj);
func3(obj);
```

# 操作符重载
