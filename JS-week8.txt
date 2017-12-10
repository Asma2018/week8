let arr = [], arr2 = [];
for (let i = 1; i <= 1000; i++) {
         arr.push(i);
}
Console.log("Array 1");
Console.log(arr);
Console.log("------------------------");
 
for (let i = 1; i <= 36; i++) {
                 arr2.push(i);
}
Console.log("Array 2 [1-36]");
Console.log(arr2);
Console.log("------------------------");
// here please start your solution
// using closures, functions and (map,filter,reduce)
const divisibleFactory = function (arr) {
         divisibleArr = function (x) {
                 var f = arr.filter(function (i) { return i % x == 0; });
                 return f.length;
         }
         return divisibleArr;     
}
 
 
var divid =  divisibleFactory(arr);
var rs = arr2.map(a=>divid(a));
Console.log("Array 2 result");
console.log(rs);