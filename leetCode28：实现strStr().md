![在这里插入图片描述](https://img-blog.csdnimg.cn/20210524200527623.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210524200535499.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)
代码演示：

```javascript
    var strStr = function(haystack, needle) {
        if(needle == '') return 0; // 如果输入needle是空的情况，直接结束运行返回0

        var arr = needle.split(''); // 将needle拆分为一个数组

        var array =  haystack.split(''); // 将haystack拆分为数组
        var result=-1; // 初始化result为-1为后边做准备
        
        for(var i = 0; i < array.length; i++){
			// 寻找needle首字母在haystack中的位置 ----- 还不知道needle在haystack中是否存在
            if(array[i] == arr[0]){
            // 切取haystack 从 i 后的needle长度项
                var s = haystack.slice(i,arr.length+i);
                // 如果两者相等就说明找对了，那么就跳出循环，如果不相等只能说明hatstack第i项与needle第一项字母相同，但后面的字符串中不跟needle相同，那么就接着往下找，如果一直没找到那么result就是-1，就不会更改。
                if(s == needle){
                    result = i;
                    break;
                }
            }
        }
        // 如果result是-1，就说明haystack中没有needle，就返回-1
        // 如果result不是-1，那就说明找到了，就返回找到的字符下标
        if(result != -1){
            return result;
        }else{
            return -1;
        }
    };
```
其中用到了slice 和 split 函数，
slice是截取字符串的函数，
split是将字符串转化为数组的函数。




