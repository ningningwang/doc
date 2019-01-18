# 变量的解构赋值
# 数组
解构赋值允许指定默认值。

let [foo = true] = [];
foo // true
let [x, y = 'b'] = ['a']; // x='a', y='b'
let [x, y = 'b'] = ['a', undefined]; // x='a', y='b'

注意，ES6 内部使用严格相等运算符（===），判断一个位置是否有值。所以，只有当一个数组成员严格等于undefined，默认值才会生效。

let [x = 1] = [undefined];
x // 1
let [x = 1] = [null];
x // null

如果一个数组成员是null，默认值就不会生效，因为null不严格等于undefined。
