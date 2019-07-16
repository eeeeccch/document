### 텍스트 바인딩
```html
<p id="app">{{ message }}</p>
```

```javascript
var app = new Vue({
  el:'#app',
  data:{
    message:'Hello Vue.js'
  }
})

console.log(app.message);
```


### 반복 렌더링
```html
<ol id="app">
  <li v-for="item in list">{{ item }}</li> <!-- <li id="app" v-for="item in list"> ... error -->
</ol>
```

```javascript
var app = new Vue({
  el:'#app',
  data:{
    list:['Apple','Banana','Melon']
  }
})

console.log(app.list);
app.list.push('Water'); //add
app.list.pop('Water');  //remove
```

### 이벤트 사용하기
```html
<div id="app">
  <button type="button" v-on:click="handleClick" id="signup" class="el">button click</button>
</div>
```

```javascript
var app = new Vue({
  el:'#app',
  methods:{
    handleClick:function(event){
      console.log(event)                    //MouseEvent...
      console.log(event.target)             //<button type="button" cid="signup" lass="el">button click</button>
      console.log(event.target.type)        //button
      console.log(event.target.id)          //signup
      console.log(event.target.className)   //el
      console.log(event.target.innerHTML)   //button click
      console.log(event.target.innerText)   //button click      
    }
  }
})
```
