### useRef
> 특정 DOM을 선택해야할 때 사용

```javascript
import React, { useRef } from "react";
function RefSample() {
  const nameInput = useRef();
  const onFocus = (e) => {
    nameInput.current.focus();
  }
  return (
    <>
      <input ref={nameInput} />
      <button onClick={onFocus}>Focus</button>
    </>
  );
}
```
