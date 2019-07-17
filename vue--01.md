### 기본적인 옵션 구성
```javascript
var app = new Vue({
  //마운트할 요소(selector)
  el:'#app',
  //사용할 데이터
  data:{
    message:'hello world'
  },
  //결과 속성
  computed:{
    computedMessage:function(){
      return this.message + '!'
    }
  },
  beforeCreate:function(){
   console.log('인스턴스 생성되고 리액티브 초기화가 일어나기 전')
  },
  created:function(){
    console.log('인스턴스 생성되고 리액티브 초기화가 일어난 후')   
  },
  mounted:function(){
    console.log('인스턴스가 마운트되기 전')
  },
  beforeUpdate:function(){
    console.log('데이터가 변경되어 DOM에 적용되기 전')
  },
  updated:function(){
    console.log('데이터가 변경되어 DOM에 적용된 후')
  },
  beforeDestroy:function(){
    console.log('Vue 인스턴스가 제거되기 전')
  },
  destroyed:function(){
    console.log('Vue 인스턴스가 제거된 후')
  },
  errorCaptured:function(){
    console.log('임의의 자식 컴포넌트에서 오류가 발생했을 때')
  }, 
  methods:{
    //함수
    foo:function(){
    
    }
  }
})
```

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
      console.log(event.target.tagName)     //BUTTON
      console.log(event.target.className)   //el
      console.log(event.target.innerHTML)   //button click
      console.log(event.target.innerText)   //button click      
    }
  }
})
```

### 이벤트 수식어
- `.once      //1회 동작`
- `.capture   //우선순위 !important와 비슷` 
- `.stop      //해당 구간 멈춤`
- `.self      //클릭 당시 본인 엘리먼트일경우에만 실행`
- `.prevent   //href와 같이 선행 이벤트 무효화`




