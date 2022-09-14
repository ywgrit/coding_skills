### 类

禁用类的构造函数和赋值函数

```cpp
/** mcros.h */

/** 禁用类的拷贝构造函数和赋值函数 */
#define DISALLOW_COPY(cname)
	cname(const cname &) = delete;
	cname &operator=(const cname &) = delete;

/** 禁用类的移动构造函数和移动赋值函数 */
#define DISALLOW_MOVE(cname)
	cname(cname &&) = delete;
	cname &operator=(cname &&) = delete;






/** ReadWriter.h */

#include "mcros.h"

class ReadWriter {
 public:
    ReadWriter() = default;
	DISALLOW_COPY(ReadWriter);
};
```

