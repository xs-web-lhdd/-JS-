![在这里插入图片描述](https://img-blog.csdnimg.cn/20210530110743302.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)

```javascript
/**
 * @param {string} s
 * @return {string}
 */
var sortSentence = function(s) {
    // 字符串化为数组
    s = s.split(' ');
    // 进行排序
    s.sort((a,b) => Number(a.slice(-1)) - Number(b.slice(-1)));
    // 再换成字符串 用正则表达式删除数字
    return s.join(' ').replace(/\d/g,'');
};

```

