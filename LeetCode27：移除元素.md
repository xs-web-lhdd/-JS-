![在这里插入图片描述](https://img-blog.csdnimg.cn/20210523161629343.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)

```javascript
var removeElement = (nums, val) => {
  for (let i = 0; i < nums.length; i++) {
    if (nums[i]===val) {
      nums.splice(i, 1)
      i-- // i 要在这里减 1,因为i不减1会自动跳过删除元素的下一个元素，从下下个元素开始，所以要减1
    }
  }
  return nums.length
}

```

