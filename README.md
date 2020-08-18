## Redux

- 리덕스란? https://redux.js.org/ 참고
- 상태를 컴포넌트의 state가 아닌 외부에서 관리하기 위해 사용



## Store 데이터 가져오기

```
import { useSelector } from "react-redux";

const Component = () => {
	const user = useSelector((state) => state.user);
	
	return (
		<div>{user.displayName}</div>
	)
}

export default Component;
```



## Action Dispatch

```
import { useDispatch } from "react-redux";

import { setUser } from "@modules/user/userActions";

const Component = () => {
	const dispatch = useDispatch();
	
	return (
		<button onClick={() => dispatch(setUser({ ...updateData }))} />
	)
}

export default Component;
```

