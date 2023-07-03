# 라디오 버튼
> 라디오 버튼은 여러 개의 조건 중, 하나만을 선택하는 요소
> 라디오 기기에서 눌려있지 않은 버튼을 눌렀을 때, 먼저 눌려있던 버튼이 있다면 눌려있던 버튼의 고정이 풀려 올라오고, 누른 버튼이 고정되는 물리적 구조가 유래가 되어 붙여진 요소 이름

이름 그대로 90년대부터 2000년대 초까지 주변에서 쉽게 찾을 수 있던 카세트 라디오를 생각해 보거나 카세트 라디오가 잘 생각나지 않는다면 지금도 볼 수 있는 선풍기의 버튼을 떠올리면 이 요소의 근본에 대한 이해가 쉽다. 비슷한 요소로는 select(콤보 상자) 요소가 있다. 
|속성|내용|
|--|--|
|`role="radio"`|접근성 API를 통해 커스텀 요소를 스크린 리더에 라디오 버튼으로 전달|
|`aria-checked="boolean"`|라디오 버튼이 선택되었는가를 접근성 API를 통해 스크린 리더 사용자에게 전달|

```html
<div role="radiogroup">
	<input type="radio" name="likeFruits" role="radio" id="id1" aria-disabled="false" tabindex="0" aria-label="Apple">
	<label for="id1" aria-hidden="true">Apple</label>

	<input type="radio" name="likeFruits" role="radio" id="id2" aria-disabled="true" disabled="disabled" tabindex="-1" aria-label="Banana">
	<label for="id2" aria-hidden="true">Banana</label>

	<input type="radio" name="likeFruits" role="radio" id="id3" aria-disabled="false" tabindex="0" aria-checked="true" aria-label="Orange">
	<label for="id3" aria-hidden="true">Orange</label>
</div>
```

# 버튼
> 버튼 요소의 button은 사전적 의미로 단추를 의미하며, 기계에서의 버튼이란 무언가를 작동시키기 위한 누를 수 있는 단추
> 누룰 수 있기 때문에 물리적으로 움푹 들어가 있거나, 돌출되어며 이 점을 참고하여 웹에서의 버튼도 사용자가 누를 수 있는 요소임을 인지할 수 있도록 양갹효과나 돌출 효과, 또는 배경색과 대비되는 디자인으로 제공

|속성|내용|
|--|--|
|`role="button"`|웹에서의 버튼은 입력 서식을 모아놓은 양식(form)을 서버로 전송|
