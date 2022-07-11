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

