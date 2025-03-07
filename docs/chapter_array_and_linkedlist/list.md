---
comments: true
---

# 列表

**由于长度不可变，数组的实用性大大降低。** 在很多情况下，我们事先并不知道会输入多少数据，这就为数组长度的选择带来了很大困难。长度选小了，需要在添加数据中频繁地扩容数组；长度选大了，又造成内存空间的浪费。

为了解决此问题，诞生了一种被称为「列表 List」的数据结构。列表可以被理解为长度可变的数组，因此也常被称为「动态数组 Dynamic Array」。列表基于数组实现，继承了数组的优点，同时还可以在程序运行中实时扩容。在列表中，我们可以自由地添加元素，而不用担心超过容量限制。

## 列表常用操作

**初始化列表。** 我们通常使用 `Integer[]` 包装类和 `Arrays.asList()` 作为中转，来初始化一个带有初始值的列表。

=== "Java"

    ```java title="list.java"
    /* 初始化列表 */
    // 注意数组的元素类型是 int[] 的包装类 Integer[]
    Integer[] numbers = new Integer[] { 1, 3, 2, 5, 4 };
    List<Integer> list = new ArrayList<>(Arrays.asList(numbers));
    ```

=== "C++"

    ```cpp title="list.cpp"
    /* 初始化列表 */
    vector<int> list = { 1, 3, 2, 5, 4 };
    ```

=== "Python"

    ```python title="list.py"
    """ 初始化列表 """
    list = [1, 3, 2, 5, 4]
    ```

=== "Go"

    ```go title="list.go"

    ```

=== "JavaScript"

    ```js title="list.js"
    var list = [1, 3, 2, 5, 4];
    ```

=== "TypeScript"

    ```typescript title="list.ts"
    /* 初始化列表 */
    const list: number[] = [1, 3, 2, 5, 4];
    ```

=== "C"

    ```c title="list.c"

    ```

=== "C#"

    ```csharp title="list.cs"

    ```

**访问与更新元素。** 列表的底层数据结构是数组，因此可以在 $O(1)$ 时间内访问与更新元素，效率很高。

=== "Java"

    ```java title="list.java"
    /* 访问元素 */
    int num = list.get(1);  // 访问索引 1 处的元素

    /* 更新元素 */
    list.set(1, 0);  // 将索引 1 处的元素更新为 0
    ```

=== "C++"

    ```cpp title="list.cpp"
    /* 访问元素 */
    int num = list[1];  // 访问索引 1 处的元素

    /* 更新元素 */
    list[1] = 0;  // 将索引 1 处的元素更新为 0
    ```

=== "Python"

    ```python title="list.py"
    """ 访问元素 """
    num = list[1]  # 访问索引 1 处的元素

    """ 更新元素 """
    list[1] = 0    # 将索引 1 处的元素更新为 0
    ```

=== "Go"

    ```go title="list.go"

    ```

=== "JavaScript"

    ```js title="list.js"
    /* 访问元素 */
    var num = list[1];

    /* 更新元素 */
    list[1] = 0;
    ```

=== "TypeScript"

    ```typescript title="list.ts"
    /* 访问元素 */
    const num: number = list[1];

    /* 更新元素 */
    list[1] = 0;
    ```

=== "C"

    ```c title="list.c"

    ```

=== "C#"

    ```csharp title="list.cs"

    ```

**在列表中添加、插入、删除元素。** 相对于数组，列表可以自由地添加与删除元素。在列表尾部添加元素的时间复杂度为 $O(1)$ ，但是插入与删除元素的效率仍与数组一样低，时间复杂度为 $O(N)$ 。

=== "Java"

    ```java title="list.java"
    /* 清空列表 */
    list.clear();

    /* 尾部添加元素 */
    list.add(1);
    list.add(3);
    list.add(2);
    list.add(5);
    list.add(4);

    /* 中间插入元素 */
    list.add(3, 6);  // 在索引 3 处插入数字 6

    /* 删除元素 */
    list.remove(3);  // 删除索引 3 处的元素
    ```

=== "C++"

    ```cpp title="list.cpp"
    /* 清空列表 */
    list.clear();

    /* 尾部添加元素 */
    list.push_back(1);
    list.push_back(3);
    list.push_back(2);
    list.push_back(5);
    list.push_back(4);

    /* 中间插入元素 */
    list.insert(list.begin() + 3, 6);  // 在索引 3 处插入数字 6

    /* 删除元素 */
    list.erase(list.begin() + 3);      // 删除索引 3 处的元素
    ```

=== "Python"

    ```python title="list.py"
    """ 清空列表 """
    list.clear()

    """ 尾部添加元素 """
    list.append(1)
    list.append(3)
    list.append(2)
    list.append(5)
    list.append(4)

    """ 中间插入元素 """
    list.insert(3, 6)  # 在索引 3 处插入数字 6

    """ 删除元素 """
    list.pop(3)        # 删除索引 3 处的元素
    ```

=== "Go"

    ```go title="list.go"

    ```

=== "JavaScript"

    ```js title="list.js"
    /* 清空列表 */
    list = [];

    /* 尾部添加元素 */
    list.push(1);
    list.push(3);
    list.push(2);
    list.push(5);
    list.push(4);

    /* 中间插入元素 */
    list.splice(3, 0, 6);

    /* 删除元素 */
    list.splice(3, 1);
    ```

=== "TypeScript"

    ```typescript title="list.ts"
    /* 清空列表 */
    list.length = 0;

    /* 尾部添加元素 */
    list.push(1);
    list.push(3);
    list.push(2);
    list.push(5);
    list.push(4);

    /* 中间插入元素 */
    list.splice(3, 0, 6);

    /* 删除元素 */
    list.splice(3, 1);
    ```

=== "C"

    ```c title="list.c"

    ```

=== "C#"

    ```csharp title="list.cs"

    ```

**遍历列表。** 与数组一样，列表可以使用索引遍历，也可以使用 `for-each` 直接遍历。

=== "Java"

    ```java title="list.java"
    /* 通过索引遍历列表 */
    int count = 0;
    for (int i = 0; i < list.size(); i++) {
        count++;
    }

    /* 直接遍历列表元素 */
    count = 0;
    for (int n : list) {
        count++;
    }
    ```

=== "C++"

    ```cpp title="list.cpp"
    /* 通过索引遍历列表 */
    int count = 0;
    for (int i = 0; i < list.size(); i++) {
        count++;
    }

    /* 直接遍历列表元素 */
    count = 0;
    for (int n : list) {
        count++;
    }
    ```

=== "Python"

    ```python title="list.py"
    """ 通过索引遍历列表 """
    count = 0
    for i in range(len(list)):
        count += 1

    """ 直接遍历列表元素 """
    count = 0
    for n in list:
        count += 1
    ```

=== "Go"

    ```go title="list.go"

    ```

=== "JavaScript"

    ```js title="list.js"
    /* 通过索引遍历列表 */
    var count = 0;
    for (let i = 0; i < list.length; i++) {
        count++;
    }

    /* 直接遍历列表元素 */
    count = 0;
    for (const n of list) {
        count++;
    }
    ```

=== "TypeScript"

    ```typescript title="list.ts"
    /* 通过索引遍历列表 */
    let count = 0;
    for (let i = 0; i < list.length; i++) {
        count++;
    }

    /* 直接遍历列表元素 */
    count = 0;
    for (const n of list) {
        count++;
    }
    ```

=== "C"

    ```c title="list.c"

    ```

=== "C#"

    ```csharp title="list.cs"

    ```

**拼接两个列表。** 再创建一个新列表 `list1` ，我们可以将其中一个列表拼接到另一个的尾部。

=== "Java"

    ```java title="list.java"
    /* 拼接两个列表 */
    List<Integer> list1 = new ArrayList<>(Arrays.asList(new Integer[] { 6, 8, 7, 10, 9 }));
    list.addAll(list1);  // 将列表 list1 拼接到 list 之后
    ```

=== "C++"

    ```cpp title="list.cpp"
    /* 拼接两个列表 */
    vector<int> list1 = { 6, 8, 7, 10, 9 };
    // 将列表 list1 拼接到 list 之后
    list.insert(list.end(), list1.begin(), list1.end());
    ```

=== "Python"

    ```python title="list.py"
    """ 拼接两个列表 """
    list1 = [6, 8, 7, 10, 9]
    list += list1  # 将列表 list1 拼接到 list 之后
    ```

=== "Go"

    ```go title="list.go"

    ```

=== "JavaScript"

    ```js title="list.js"
    /* 拼接两个列表 */
    var list1 = [ 6, 8, 7, 10, 9 ];
    list.push(...list1)
    ```

=== "TypeScript"

    ```typescript title="list.ts"
    /* 拼接两个列表 */
    const list1: number[] = [6, 8, 7, 10, 9];
    list.push(...list1);
    ```

=== "C"

    ```c title="list.c"

    ```

=== "C#"

    ```csharp title="list.cs"

    ```

**排序列表。** 排序也是常用的方法之一，完成列表排序后，我们就可以使用在数组类算法题中经常考察的「二分查找」和「双指针」算法了。

=== "Java"

    ```java title="list.java"
    /* 排序列表 */
    Collections.sort(list);  // 排序后，列表元素从小到大排列
    ```

=== "C++"

    ```cpp title="list.cpp"
    /* 排序列表 */
    sort(list.begin(), list.end());  // 排序后，列表元素从小到大排列
    ```

=== "Python"

    ```python title="list.py"
    """ 排序列表 """
    list.sort()  # 排序后，列表元素从小到大排列
    ```

=== "Go"

    ```go title="list.go"

    ```

=== "JavaScript"

    ```js title="list.js"
    /* 排序列表 */
    list.sort((a, b) => a - b);  // 排序后，列表元素从小到大排列
    ```

=== "TypeScript"

    ```typescript title="list.ts"
    /* 排序列表 */
    list.sort((a, b) => a - b);  // 排序后，列表元素从小到大排列
    ```

=== "C"

    ```c title="list.c"

    ```

=== "C#"

    ```csharp title="list.cs"

    ```

## 列表简易实现 *

为了帮助加深对列表的理解，我们在此提供一个列表的简易版本的实现。需要关注三个核心点：

- **初始容量：** 选取一个合理的数组的初始容量 `initialCapacity` 。在本示例中，我们选择 10 作为初始容量。
- **数量记录：** 需要声明一个变量 `size` ，用来记录列表当前有多少个元素，并随着元素插入与删除实时更新。根据此变量，可以定位列表的尾部，以及判断是否需要扩容。
- **扩容机制：** 插入元素有可能导致超出列表容量，此时需要扩容列表，方法是建立一个更大的数组来替换当前数组。需要给定一个扩容倍数 `extendRatio` ，在本示例中，我们规定每次将数组扩容至之前的 2 倍。

本示例是为了帮助读者对如何实现列表产生直观的认识。实际编程语言中，列表的实现远比以下代码复杂且标准，感兴趣的读者可以查阅源码学习。

=== "Java"

    ```java title="my_list.java"
    /* 列表类简易实现 */
    class MyList {
        private int[] nums;           // 数组（存储列表元素）
        private int capacity = 10;    // 列表容量
        private int size = 0;         // 列表长度（即当前元素数量）
        private int extendRatio = 2;  // 每次列表扩容的倍数

        /* 构造函数 */
        public MyList() {
            nums = new int[capacity];
        }

        /* 获取列表长度（即当前元素数量）*/
        public int size() {
            return size;
        }

        /* 获取列表容量 */
        public int capacity() {
            return capacity;
        }

        /* 访问元素 */
        public int get(int index) {
            // 索引如果越界则抛出异常，下同
            if (index >= size)
                throw new IndexOutOfBoundsException("索引越界");
            return nums[index];
        }

        /* 更新元素 */
        public void set(int index, int num) {
            if (index >= size)
                throw new IndexOutOfBoundsException("索引越界");
            nums[index] = num;
        }

        /* 尾部添加元素 */
        public void add(int num) {
            // 元素数量超出容量时，触发扩容机制
            if (size == capacity())
                extendCapacity();
            nums[size] = num;
            // 更新元素数量
            size++;
        }

        /* 中间插入元素 */
        public void insert(int index, int num) {
            if (index >= size)
                throw new IndexOutOfBoundsException("索引越界");
            // 元素数量超出容量时，触发扩容机制
            if (size == capacity())
                extendCapacity();
            // 将索引 index 以及之后的元素都向后移动一位
            for (int j = size - 1; j >= index; j--) {
                nums[j + 1] = nums[j];
            }
            nums[index] = num;
            // 更新元素数量
            size++;
        }

        /* 删除元素 */
        public int remove(int index) {
            if (index >= size)
                throw new IndexOutOfBoundsException("索引越界");
            int num = nums[index];
            // 将索引 index 之后的元素都向前移动一位
            for (int j = index; j < size - 1; j++) {
                nums[j] = nums[j + 1];
            }
            // 更新元素数量
            size--;
            // 返回被删除元素
            return num;
        }

        /* 列表扩容 */
        public void extendCapacity() {
            // 新建一个长度为 size 的数组，并将原数组拷贝到新数组
            nums = Arrays.copyOf(nums, capacity() * extendRatio);
            // 更新列表容量
            capacity = nums.length;
        }
    }
    ```

=== "C++"

    ```cpp title="my_list.cpp"
    /* 列表类简易实现 */
    class MyList {
    private:
        int* nums;                // 数组（存储列表元素）
        int numsCapacity = 10;    // 列表容量
        int numsSize = 0;         // 列表长度（即当前元素数量）
        int extendRatio = 2;      // 每次列表扩容的倍数

    public:
        /* 构造函数 */
        MyList() {
            nums = new int[numsCapacity];
        }

        /* 获取列表长度（即当前元素数量）*/
        int size() {
            return numsSize;
        }

        /* 获取列表容量 */
        int capacity() {
            return numsCapacity;
        }

        /* 访问元素 */
        int get(int index) {
            // 索引如果越界则抛出异常，下同
            if (index >= size())
                throw out_of_range("索引越界");
            return nums[index];
        }

        /* 更新元素 */
        void set(int index, int num) {
            if (index >= size())
                throw out_of_range("索引越界");
            nums[index] = num;
        }

        /* 尾部添加元素 */
        void add(int num) {
            // 元素数量超出容量时，触发扩容机制
            if (size() == capacity())
                extendCapacity();
            nums[size()] = num;
            // 更新元素数量
            numsSize++;
        }

        /* 中间插入元素 */
        void insert(int index, int num) {
            if (index >= size())
                throw out_of_range("索引越界");
            // 元素数量超出容量时，触发扩容机制
            if (size() == capacity())
                extendCapacity();
            // 索引 i 以及之后的元素都向后移动一位
            for (int j = size() - 1; j >= index; j--) {
                nums[j + 1] = nums[j];
            }
            nums[index] = num;
            // 更新元素数量
            numsSize++;
        }

        /* 删除元素 */
        int remove(int index) {
            if (index >= size())
                throw out_of_range("索引越界");
            int num = nums[index];
            // 索引 i 之后的元素都向前移动一位
            for (int j = index; j < size() - 1; j++) {
                nums[j] = nums[j + 1];
            }
            // 更新元素数量
            numsSize--;
            // 返回被删除元素
            return num;
        }

        /* 列表扩容 */
        void extendCapacity() {
            // 新建一个长度为 size * extendRatio 的数组，并将原数组拷贝到新数组
            int newCapacity = capacity() * extendRatio;
            int* extend = new int[newCapacity];
            // 将原数组中的所有元素复制到新数组
            for (int i = 0; i < size(); i++) {
                extend[i] = nums[i];
            }
            int* temp = nums;
            nums = extend;
            delete[] temp;
            numsCapacity = newCapacity;
        }
    };
    ```

=== "Python"

    ```python title="my_list.py"
    """ 列表类简易实现 """
    class MyList:
        """ 构造函数 """
        def __init__(self):
            self.__capacity = 10                 # 列表容量
            self.__nums = [0] * self.__capacity  # 数组（存储列表元素）
            self.__size = 0                      # 列表长度（即当前元素数量）
            self.__extend_ratio = 2              # 每次列表扩容的倍数

        """ 获取列表长度（即当前元素数量） """
        def size(self):
            return self.__size
        
        """ 获取列表容量 """
        def capacity(self):
            return self.__capacity
        
        """ 访问元素 """
        def get(self, index):
            # 索引如果越界则抛出异常，下同
            assert index < self.__size, "索引越界"
            return self.__nums[index]

        """ 更新元素 """
        def set(self, num, index):
            assert index < self.__size, "索引越界"
            self.__nums[index] = num

        """ 中间插入（尾部添加）元素 """
        def add(self, num, index=-1):
            assert index < self.__size, "索引越界"
            # 若不指定索引 index ，则向数组尾部添加元素
            if index == -1:
                index = self.__size
            # 元素数量超出容量时，触发扩容机制
            if self.__size == self.capacity():
                self.extend_capacity()
            # 索引 i 以及之后的元素都向后移动一位
            for j in range(self.__size - 1, index - 1, -1):
                self.__nums[j + 1] = self.__nums[j]
            self.__nums[index] = num
            # 更新元素数量
            self.__size += 1

        """ 删除元素 """
        def remove(self, index):
            assert index < self.__size, "索引越界"
            # 索引 i 之后的元素都向前移动一位
            for j in range(index, self.__size - 1):
                self.__nums[j] = self.__nums[j + 1]
            # 更新元素数量
            self.__size -= 1

        """ 列表扩容 """
        def extend_capacity(self):
            # 新建一个长度为 self.__size 的数组，并将原数组拷贝到新数组
            self.__nums = self.__nums + [0] * self.capacity() * (self.__extend_ratio - 1)
            # 更新列表容量
            self.__capacity = len(self.__nums)
    ```

=== "Go"

    ```go title="my_list.go"

    ```

=== "JavaScript"

    ```js title="my_list.js"
    /* 列表类简易实现 */
    class MyList {
        nums;           // 数组（存储列表元素）
        _capacity = 10;    // 列表容量
        _size = 0;         // 列表长度（即当前元素数量）
        extendRatio = 2;  // 每次列表扩容的倍数

        /* 构造函数 */
        constructor() {
            this.nums = new Array(this._capacity);
        }

        /* 获取列表长度（即当前元素数量）*/
        get size() {
            return this._size;
        }

        /* 获取列表容量 */
        get capacity() {
            return this._capacity;
        }

        /* 访问元素 */
        get(index) {
            // 索引如果越界则抛出异常，下同
            if (index >= this._size)
                throw new Error("索引越界");
            return this.nums[index];
        }

        /* 更新元素 */
        set(index, num) {
            if (index >= this._size)
                throw new Error("索引越界");
            this.nums[index] = num;
        }

        /* 尾部添加元素 */
        add(num) {
            //元素数量超出容量时，触发扩容机制
            if (this._size === this._capacity)
                this.extendCapacity();
            this.nums[this._size] = num;
            // 更新元素数量
            this._size++;
        }

        /* 中间插入元素 */
        insert(index, num) {
            if (index >= this._size)
                throw new Error("索引越界");
            // 元素数量超出容量时，触发扩容机制
            if (this._size === this._capacity)
                this.extendCapacity();
            // 将索引 index 以及之后的元素都向后移动一位
            for (let j = this._size - 1; j >= index; j--) {
                this.nums[j + 1] = this.nums[j];
            }
            this.nums[index] = num;
            // 更新元素数量
            this._size++;
        }

        /* 删除元素 */
        remove(index) {
            if (index >= this._size)
                throw new Error("索引越界");
            let num = this.nums[index];
            // 将索引 index 之后的元素都向前移动一位
            for (let j = index; j < this._size - 1; j++) {
                this.nums[j] = this.nums[j + 1];
            }
            // 更新元素数量
            this._size--;
            // 返回被删除元素
            return num;
        }

        /* 列表扩容 */
        extendCapacity() {
            // 新建一个长度为 size 的数组，并将原数组拷贝到新数组
            this.nums = this.nums.concat(
                new Array(this.capacity * (this.extendRatio - 1))
            );
            // 更新列表容量
            this._capacity = this.nums.length;
        }

        /* 将列表转换为数组 */
        toArray() {
            let size = this.size;
            // 仅转换有效长度范围内的列表元素
            let nums = new Array(size);
            for (let i = 0; i < size; i++) {
                nums[i] = this.get(i);
            }
            return nums;
        }
    }
    ```

=== "TypeScript"

    ```typescript title="my_list.ts"
    /* 列表类简易实现 */
    class MyList {
        private nums: Array<number>; // 数组（存储列表元素）
        private _capacity: number = 10; // 列表容量
        private _size: number = 0; // 列表长度（即当前元素数量）
        private extendRatio: number = 2; // 每次列表扩容的倍数

        /* 构造函数 */
        constructor() {
            this.nums = new Array(this._capacity);
        }

        /* 获取列表长度（即当前元素数量）*/
        public size(): number {
            return this._size;
        }

        /* 获取列表容量 */
        public capacity(): number {
            return this._capacity;
        }

        /* 访问元素 */
        public get(index: number): number {
            // 索引如果越界则抛出异常，下同
            if (index >= this._size) {
                throw new Error('索引越界');
            }
            return this.nums[index];
        }

        /* 更新元素 */
        public set(index: number, num: number): void {
            if (index >= this._size) throw new Error('索引越界');
            this.nums[index] = num;
        }

        /* 尾部添加元素 */
        public add(num: number): void {
            // 如果长度等于容量，则需要扩容
            if (this._size === this._capacity) {
                this.extendCapacity();
            }
            // 将新元素添加到列表尾部
            this.nums[this._size] = num;
            this._size++;
        }

        /* 中间插入元素 */
        public insert(index: number, num: number): void {
            if (index >= this._size) {
                throw new Error('索引越界');
            }
            // 元素数量超出容量时，触发扩容机制
            if (this._size === this._capacity) {
                this.extendCapacity();
            }
            // 将索引 index 以及之后的元素都向后移动一位
            for (let j = this._size - 1; j >= index; j--) {
                this.nums[j + 1] = this.nums[j];
            }
            // 更新元素数量
            this.nums[index] = num;
            this._size++;
        }

        /* 删除元素 */
        public remove(index: number): number {
            if (index >= this._size) throw new Error('索引越界');
            let num = this.nums[index];
            // 将索引 index 之后的元素都向前移动一位
            for (let j = index; j < this._size - 1; j++) {
                this.nums[j] = this.nums[j + 1];
            }
            // 更新元素数量
            this._size--;
            // 返回被删除元素
            return num;
        }

        /* 列表扩容 */
        public extendCapacity(): void {
            // 新建一个长度为 size 的数组，并将原数组拷贝到新数组
            this.nums = this.nums.concat(
                new Array(this.capacity() * (this.extendRatio - 1))
            );
            // 更新列表容量
            this._capacity = this.nums.length;
        }
    }
    ```

=== "C"

    ```c title="my_list.c"

    ```

=== "C#"

    ```csharp title="my_list.cs"

    ```
