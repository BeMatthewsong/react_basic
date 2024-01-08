# 서버 데이터를 GET하기 위한 훅, useQuery

useQuery()에서 쿼리란 '문의하다, 질문하다'라는 뜻을 가지고 있는 단어입니다. <br/>
데이터베이스 같은 것에 우리가 필요한 데이터를 요청하는 것을 말합니다. <br/>
즉, useQuery()는 필요한 데이터를 백엔드에 요청해서 받아 오는 React Hook입니다.


```jsx
const result = useQuery({queryKey: ['keyword'], queryFn: func};
```

## 다양한 상태 정보

data : 
