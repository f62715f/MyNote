### 註解

##### 用法

* // 內容

只能用一行
   
* /\*內容\*/ 

可以框整行，就是可以換行的意思

---

### variable 變量

方便給內存地址取名
   
e.g.   a = 5, 實際是將0x000...指定為a

   ```cpp
   // 變量類型 變量名稱 = 存取數據
   int a = 6
   ```

---

### 常量

用於規定一個不能動的數據

##### 用法

* define     數據類型     數據               <注意：不可有逗號>

* const      數據類型   =   數據  ;
```cpp
#define Week 7 
// 注意 #define 後面不可有逗號

int main()
{

    cout << "一週有" << Week << "天" << endl ;

    const int Month = 30 ;  // const 為常量，不可動

    cout << "一個月有" << Month << "天" << endl ;

    return 0 ;
}
```


---

### **iostream與stdio的區別**

    **stdio**屬於c語言，開發c程式用stdio，輸入輸出格式為printf()，scanf()

    **iostream**屬於c++語言，開發c++程式可以用stdio和iostream，推薦使用 iostream，輸入輸出格式為count<<..，cin>>..

```c
#include <stdio.h>

int main(){
    printf("Hello, World!\n");
    return 0;
}
```
