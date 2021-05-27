![在这里插入图片描述](https://img-blog.csdnimg.cn/20210526210023931.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUyMjA3NzI4,size_16,color_FFFFFF,t_70#pic_center)

```javascript
/**
 * @param {string[]} strs
 * @return {string}
 */
var longestCommonPrefix = function(strs) {
    // 数组为空直接返回
    if(strs.length == 0) return "";

    // 选出数组的第一个元素 --- 默认它就是要找的公共前缀
    let ans = strs[0];

// 用循环 --- 使默认的公共前缀跟数组的每一个元素进行比较 
    for(let i =1;i<strs.length;i++) {
        // var result;
        let j=0;
        for(;j<ans.length && j < strs[i].length;j++) {
            // 如果选出来的元素的第j个字母与比较的元素的第j个字母不一致就跳出循环,并标记j
            if(ans[j] != strs[i][j])
                // result = j;
                break;
        }
        // 将默认的公共前缀进行更新
        ans = ans.substr(0, j);

        // 如果默认的公共前缀更新到为空，就代表着没有公共前缀就返回""不再进行循环了
        if(ans === "")
            return ans;
    }
    return ans;
};
```

