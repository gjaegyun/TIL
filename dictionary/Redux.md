# Redux 간단 정리

Redux 쓰는 이유(component간 state공유 편리)

### Redux store에 state 보관 방법
    ``` js
    let user = createSlice({
        name : state의 이름
        initialState : state의 값
    })

    export default configureStore({
        reducer: {
            작명 : state의 이름.reducer
        }
    })
    ```

### Redux store
    ``` jsx
    let a = useSelector((state)=>{ return state })
    //Redux store에 있던 state 모든것이 담긺
    //원하는 것 골라서 사용하고 싶다면 .찍어서 사용
    ```

### Redux의 state 변경하는 방법

    state 수정 함수 만들기

    ``` jsx
    let user = createSlice({
        name : state의 이름
        initialState : state의 값

        reducers : {
            함수(){
                retrun 
            }
        }
    })

    export let { 함수 } user.actions //object 형식으로 담김
    ```

### Redux 이용해서 state 사용법

**useDispatch** 사용

    dispatch(state변경함수()) 이렇게 해야지만 state변경함수가 동작한다.

    dispatch가 하는 역할은 useDispatch를 dispatch안에 담아서 dispatch가 괄호 안에 있는 함수가 포함되어 있는 파일에 요청을 보내는 것이다.

    