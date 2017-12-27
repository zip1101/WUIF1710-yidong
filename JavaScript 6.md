
* sort 实现数组排序的功能，会影响数据本身的
## ES3 兼容IE678..这些浏览器
* push 在数组的末尾添加一个或者多个元素 
* 返回值 新数组的长度
```
  var arr=[1,2,3,4,5,"asd"];
  var newarr=[];
  for (var i=0; i<arr.lengrh;i++){
      if(typeof arr[i]==="number"){
        newarr.push(arr[i])
      }
   }
    console.log(arr);
    
(6) [1, 2, 3, 4, 5, "asd"]
```   
* pop()删除掉数组的最后一个元素只能删掉一个
* 返回值 删除的元素内容
```
  var r = arr.pop();
  console.log(arr);
  console.log(r);
  
  asd
```
* unshift() 在数组的开始位置添加一个或者多个元素
* 返回值 新的数组长度
```
 var r=arr.unshift(1,1,0);
 console.log(arr);
 console.log(r);
 
(9) [1, 1, 0, 1, 2, 3, 4, 5, "asd"]
 9
```
* shift() 在数组的开始位置删除一个元素
* 返回值 删除元素的内容
```
  var r=arr.shift();
  console.log(arr);
  console.log(r);
  
  (5) [2, 3, 4, 5, "asd"]
   1
```
* splice（）万能的添加删除方法
* 第一个参数 操作的位置
* 第二个参数  要删除的个数
* 后续的参数  表示要添加的内容
* 返回值 删除的元素组成的数组
```
   var arr3=newarr.splice(1,2);
    console.log(newarr);
    console.log(arr3);
    
    (3) [1, 4, 5]
    (2) [2, 3]
```
* slice() 从数组中截取指定内容返回不会影响原数组 
* 返回值 起始位置为数组的实际下标 结束位置的实际下标为结束数值减1
如果是负数， 则用数组的长度加上该值确定位置
```
var num1=[1,2,3,4];
var str=num1.slice(0,3);
console.log(str); 

(3) [1, 2, 3]
```
* sort() 实现数组排序的功能，会影响数组本身的，实现个位数排序是没有问题的 但是还需要更深层次的处理
```
var arr=[1,1,1,2,3,2,3,4,8,4,7];
sort中的函数就是它的处理
arr.sort(function(a,b){
	if(a>b){
		return 1;
	}else if(a<b){
		return -1;
	}
});
console.log(arr);

(11) [1, 1, 1, 2, 2, 3, 3, 4, 4, 7, 8]
```
```
var arr=[
    {name:"zhangsan",grad:87},
    {name:"lisi",grad:99},
    {name:"wangwu",grad:90},
    ];
arr.sort(function(a,b){
   i( a.grad>b.grad){
        return 1;
    }else{
        return -1;
    }
   
})
 console.table(arr);
``` 
* reverse 将数组中的内容反向展示
 ```
    arr.reverse();
    console.log(arr);
    
(11) [8, 7, 4, 4, 3, 3, 2, 2, 1, 1, 1]
```
* concat 将多个数组合并成一个 它对于原数组是没有任何影响的 需要返回值
```
var num1=[1,2,3,4];
var num2=[5,6,7,8];
var newnum=num1.concat(num2);
console.log(newnum);

(8) [1, 2, 3, 4, 5, 6, 7, 8]
```
* join() 将数组转化为字符串  本身数组是不会发生变化的 元素是通过指定的分隔符进行分隔的    
* 返回值 输出之后就会显示转成字符串之后的数组
```
    var str=arr.join( , )
    console.log(str);
```
## ES5兼容IE9 IE10...
* reduce 累加器 
*  reduce(function(a,b){
*      
*  }); 从左往右加
```
    var arr=[1,2,3,4,5];
    var num=arr.reduce( function(a,b){
     return a.concat(b);
        console.log(a,b);
    }，arr);
     console.log(newarr);
    
    var newarr=arr.reduceRight(function(a,b){
        return a.concat(b);
    }, arr);
    console.log(newarr);
```
* reduceright 从右往左加

## ES6 可能有一些新版本浏览器都不支持
#### forEach filter map some every indexOf  lastIndexOf reduce reduceRight
* indexOf 获取数组中某个值第一次出现位置的下标
* lastIndexOf 获取数值中某个值最后一次出现位置的下标
```
var arr=[1,2,3,4,5,1,2,3,4,5];
 console.log(arr.indexOf(1));
 
 0
```
```
 console.log(arr.lastIndexOf(1)); 
 
 5
```
* find() 根据我们设置的条件进行查找，如果有满足条件的，就把这个值返回
``` 
    console.clear();
var arr=[   
{name:"zhangsan",grad:87},
{name:"lisi", grad:99},
{name:"wangwu",grad:90},
];
 var r=arr.find(function(v,i){
     if(v.grade===90){
          return true;
 }
 });
 console.log(r);
```        
* findIndex() 根据我们设置的条件查找，如果有满足条件的，
* fill() 对于数组进行填充 把数组在的空值填充为某个值
```
var r=arr.findIndex(function(v,i){
      if(v.grade===90){
          return true;
    }
  });
    console.log(r);
```

var arr =new array(10);
arr.fill(1);
console.log(arr);
```
* copyWithin() 用数组的某一部分替换掉另一部分
```
 var arr= [1,2,3,4,5];
 arr.copyWithin(0,2);
 console.log(arr);
```
* includes() 用来判断数组中是否包含某个值的方法

```
    console.log(arr.includes(3));
```
* Array() 
```
 console.log(Array.isarray(111));
```
* Array.from()  把一个类数组(有length的对象)转化为真正的数组

```

  function fn(){
      console.log(Array.from(arguments));
  }
  fn(1,2,3,4,5);
  Array.from();
  var arr=new Array(5,6,7);
  var arr=Array.of(5,6,7);
  console.log(arr);
```


## 原生对象
## 宿主对象
## BOM
##  DOM
## Document 对象
## 每一个标签
```
* console.log(document);
* console.dir(document);
*  属性
*  console.log(docmument.title);
*  document.title="hello";
*  url
*  console.log(document.URL);
*  console.dir(document.body);
*  all
*  console.log(document.all);
*  images
*  console.log(document.images);
*  links
*  console.log(document.links);
*  anchors 获取的是锚点 a标签
*  console.log(document.anchors);
*  方法:
*  querySelector(选择器);
  根据我们传入的选择器,获取到页面中对应的元素的对象
*  querySelectorAll(选择器)；
  根据我们传入的选择器,获取到页面中对应的与元素的集合
```
  var divObj=document.querySelector(".one");
 
  var divs=doument.querySelcetaAll"(.one");
```