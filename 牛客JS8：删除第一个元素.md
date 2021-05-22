![在这里插入图片描述](https://img-blog.csdnimg.cn/20210522204337437.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)

```javascript
function prepend(arr, item) {
            var array;
            // console.log(array);
            [...array] = arr;
            // console.log(array);
            array.unshift(item);
            return array;
}
```

