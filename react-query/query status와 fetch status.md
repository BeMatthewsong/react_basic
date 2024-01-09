## query status
`query status`는 실제로 받아온 data 값이 있는지 없는지를 나타내는 상태 값이다. <br/>
`query status`는 `useQuery()` 결괏값에서 `status` 값을 통해 확인할 수 있다.

### query status의 세 가지 상태
- pending : 데이터를 아직 받아오지 못한 상태
- error : 데이터를 받아오는 중에 에러가 발생한 상태
- sucess : 데이터를 성공적으로 받아온 상태


##### useQuery를 콘솔로 출력한 상태
  ![image](https://github.com/BeMatthewsong/react_basic/assets/98685266/5ad94d3c-4c50-41ff-9d58-0b0016d1d1e6)



## fetch status 
`fetch status`는 queryFn() 함수의 실행 상태이다. <br/>
`fetch status`는 `fetchStatus`를 통해 확인할 수 있다.

### fetch status의 세 가지 상태
- fetching : 현재 쿼리 함수가 실행되고 있는 중
- paused : 쿼리 함수가 시작했다가 실제로 실행되지 않는 상태 (네트워크 오류)
- idle : fetching이나 paused가 아닌 상태

![image](https://github.com/BeMatthewsong/react_basic/assets/98685266/48f0d318-1e4c-4f60-9d53-04599a50bb03)

위 그림처럼 query status와 fetch status는 엄연히 독립적인 상태이다.
`"pending & fetching"` 상태에서 `"success & idle"` 상태가 되겠지만, 
에러가 발생하는 경우 `"error & idle"` 상태가 될 수도 있다.
`"success & idle"` 상태에서 데이터를 refetch하게 되면 `"success & fetching"` 상태가 되기도 합니다
