# 함수형 프로그래밍

### currying

    ```
    const order = store => (menu) => {
        console.log(`${store} - ${menu}`);
    }

    ~~~ > Es5 변환

    function order(store){
        return function(menu){
            console.log(`${store} - ${menu}`);
        }
    }

    ~~~ > 사용
    const orderChina = order("중국집");
    => orderChina의 return type은 function 이므로 orderChina("자장면") 이렇게 사용
    ```
    
    - 위와 같은 패턴은 js로 게임을 만들경우 자주 사용.(게임은 설치형이기 때문에)
    
<hr/>

### composition
    - 여러개의 함수 중 리팩토링이 필요할 경우 쪼개서 사용
    ```
    f1 : fullName()
    f2 : appendAddr()
    f3 : removeAddr()

    const data = compose(fullName, appendAddr, removeAddr)(user);

    const compose = (...fns) => (obj) => {
        fns.reduce((temp , fn) => fn(C), obj );
    }
    - 3개의 인자를 주면 arguments가 Array 형태로 변경됨.

    const fullName = (user) => ({
        ...user, fullName: `${userFirstName} ${userLastName}`
    })
    ```

