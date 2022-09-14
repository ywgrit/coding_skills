### 类

禁用类的构造函数和拷贝构造函数

```cpp
/** mcros.h */
#define DISALLOW_COPY(cname)
	cname(const cname &) = delete;
	cname &operator=(const cname &) = delete;
```

禁用类的移动构造函数和移动赋值函数

```cpp
/** mcros.h */
#define DISALLOW_MOVE(cname)
	cname(cname &&) = delete;
	cname &operator=(cname &&) = delete;
```



使用

```cpp
/** ReadWriter.h */
#include "mcros.h"

class ReadWriter {
 public:
	DISALLOW_COPY(ReadWriter);
};
```

