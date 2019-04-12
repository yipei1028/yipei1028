# 那些我在LeetCode學到的小事:ep1
###### tags: `leetCode` `peiNote` `forEach` `reverse` `bitwiseOperator`
純粹是個人的筆記，希望你比我聰明。

### [看題目點我](https://leetcode.com/problems/flipping-an-image/)：

[reverse()](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse)
- 會**改變**原本的陣列

[forEach()](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
- **不會回傳值**，硬要 return 會得到 undefined
- 可以把 forEach 想成取代 for 迴圈的功能，因此不會改變原本的陣列
- 使用 forEach，如果想要改變特定index的值，**不能直接reassign**，要在參數中傳入 index 和自己語法如下:
```javascript
arr.forEach(function(part, index, theArray) {
  theArray[index] = "hello world";
});
```
我自己對一開始很直覺的想直接 assign 值，給 foreach 當前的值像這樣：
```javascript
var arr = ["one","two","three"];

arr.forEach(function(part) {
  part = "four";
})

//arr = ["one","two","three"]
```
在 arr 是 primitive type 的情況下， arr 的值並不會被 'four' 賦值，是因為每一次我們跑進 foreach 裡面改掉的是 `part` 這個變數，而不是 `arr[index]`，原文如下：

> So for your code above, this means that each time the forEach() iterates, part is equal to the same value as arr[index], but not the same object.

如果想要更改 foreach 當前的值，還是謹慎地使用  `arr[index]` 比較好！

^ (Bitwise XOR Operator)
- Sets each bit to 1 if only one of two bits is 1

![](https://i.imgur.com/4wSNX1x.png)

![](https://i.imgur.com/RqyW2Jr.png)


別人的答案長這樣，然後讓我困惑`^`這個小耳朵究竟是什麼？
```javascript
var flipAndInvertImage = function(A) {
    A.forEach(outer => {
        outer.reverse();
        outer.forEach((inner, index) => outer[index] = inner ^ 1);
    });
    return A;
};
```


### 參考
https://stackoverflow.com/questions/12482961/is-it-possible-to-change-values-of-the-array-when-doing-foreach-in-javascript/12482991

##### 2019/04/11
