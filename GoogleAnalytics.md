# Google Tag API
- [config](#config)
- [get](#get)
- set
- event
- consent
- 매개변수범위
- 매개변수 우선순위

## config
> 제품의 구성을 설정할수 있으며, 한번만 구성하면 됨

```javascript
// <TARGET_ID>는 Google Analytics의 고유 식별자
// <additional_config_info>는 하나 이상의 매개변수-값 쌍
gtag('config', '<TARGET_ID>', {additional_config_info});

// <TAG_ID>는 특정 Google 태그를 로드하기 위해 페이지에 배치하는 식별자
gtag('config','<TAG_ID>');

// 추가 구성 정보를 전송하는 예시
gtag('config','<TAG_ID>',{
  'send_page_view': false,
  'groups': 'agency'
});
```

## get
```javascript
// gtag.ja에서 제공하는 다양한 값을 가져올수 있음
gtag('get','<target>',field_name',callback)

//프로미스로 값 가져오기
const gclidPromise = new Promise(resolve => {
  gtag('get','DC-XXXXXXX','gclid',resolve)
});
gclidPromise.then((gclid) =>{
  // Do something
});

//측정 프로토콜에 이벤트 전송하기
gtag('get','UA-XXXXXXX-Y','client_id',(clientID) =>{
  sendOfflineEvent(clientID, 'tutorial_begin')
});
function sendOfflineEvent(clientID, eventName, eventData) {
  // Send necessary data to your server...
}

//설정한 값 가져오기
gtag('set', {currency: 'USD'});
gtag('get', 'UA-XXXXXXXX-Y', 'currency', (currency) => {
  // Do something with currency value you set earlier.
});
```
인수|유형|예|설명
--|--|--|--
`<target>`|string|UA-XXXXXXX-Y|값을 가져올 대상
`<field_name>`|FieldName|client_id|가져올 필드의 이름
callback|Function|(field) => console.log(field)|요청된 필드를 사용해 호출될 함수
> FieldName은 `gtag('set')`명령어로 설정한 맞춤 필드의 이름
