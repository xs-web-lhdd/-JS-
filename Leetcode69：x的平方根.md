本人太菜了，哎！算法真的拉跨，无奈只能刷一些简单题目，望有一日成为算法大佬......
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210603211829988.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)

```javascript
/**
 * @param {number} x
 * @return {number}
 */
var mySqrt = function(x) {
    var i = 1;
    var result;
    while(true){
        if(i * i == x){
            return i;
        }
        if(i*i > x){
            result = i;
            break;
        }
        i++;
    }
    // return result;
    if(result*result > x ){
        return result-1;
    }else{
        return result;
    }
};
```

