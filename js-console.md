```javascript
//level
console.log('log')      //개발 - 출력
console.info('info')    // 정보
console.warn('warn')    // 경보
console.error('error')  // 에러

//assert
console.assert(2=== 3, 'not same!');
console.assert(2===2, 'same!');

//print
console.log();
console.table(obj);
console.dir(obj,{colors:false, depth:0 });

//measuring time
console.time();
for (let i = 0; i<1000; i++){
  i++
}
console.timeEnd();

//counting
console.count();
console.countReset();
```
