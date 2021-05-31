## 含泪错4次！！！
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210531221906438.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)

```javascript
/**
 * @param {number[]} digits
 * @return {number[]}
 */
var plusOne = function(digits) {


//化为数字写法：行不通
    // 定义数组的和 s
    // let s = 0;

    // // 利用循环将数组中的单个项化为数字加在一起 ------ 这种写法会失真
    // for(var i = 0; i < digits.length; i++){
    //     s = s + digits[i]*Math.pow(10,digits.length-i-1);
    // }

    // // 将数字加一
    // s = s + 1;
    // // 将数字类型化为字符串类型
    // s = s.toString();
    // // 返回数组
    // return s.split('');

    for(let i = digits.length-1;i>=0;i--){
        if(digits[i] !==9){
            // 最后一位是0~8
            digits[i]++
                return digits; // 结束程序
        }else{
            // 是 9
            digits[i] = 0 
        }
    }

// 当数组是[9,9,9,9]类似这种写法时:经过上面循环全部变成[0,0,0,0]的形式
    // 用展开运算符
    let result = [1,...digits];
    
    return result;

};
```

```javascript
注意：[9,9,9,9]这种不要忽略了
```

