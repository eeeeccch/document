### toLocalString()
```javascript
function comma(x){
  return x.toLocaleString('ko-KR');
}

comma(123456789); //123,456,789
```
> 숫자 콤마 처리

### setInterval() & clearInterval()
```javascript
var loop = setInterval(data,time);
clearInterval(loop);
```

```javascript
var valid = {
	'tel_old': /(\d{3})(\d{3})(\d{4})/,
	'tel_new': /(\d{3})(\d{4})(\d{4})/,
	'card_num': /(\d{4})(\d{4})(\d{4})(\d{4})/,
	'email': /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/g;
	'pwd': /^.*(?=.{8,10})(?=.*[a-zA-Z])(?=.*?[A-Z])(?=.*\d)(?=.+?[\W|_])[a-zA-Z0-9!@#$%^&*,
	'ip': /^(?!.*\.$)((?!0\d)(1?\d?\d|25[0-5]|2[0-4]\d)(\.|$)){4}$/g,
	'onlyNum': /^[0-9]+$/g.test(1234),
	'onlyEnd': /^[a-zA-Z]+$/g.test("abcd"),
	'onlyKor': /^[가-힣]+$/g.test("가나다라"),
	'tagRemove': /<[^>]*>/g,
}
```