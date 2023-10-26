# MongoDB

## 목적
- MySQL에서 대량 insert로 인한 부하되는 요소를 MongoDB를 사용하여 해결하기 위함

## 방법
- 불필요한 index 만들지 않기
- index prefix를 사용하기
  - compound index를 만들면 prefix가 동일한 index는 만들지 않아도 됨
- multi sorting
  - compound index 순서와 동일하게 나열되어야 함
  - ![MongoDB MultingSorting.png](image%2FMongoDB%20MultingSorting.png)
  - ![몽고DB 멀티소팅 Correct 예제.png](image%2F%EB%AA%BD%EA%B3%A0DB%20%EB%A9%80%ED%8B%B0%EC%86%8C%ED%8C%85%20Correct%20%EC%98%88%EC%A0%9C.png)
  - ![몽고DB 멀티소팅 Not Correct 예제.png](image%2F%EB%AA%BD%EA%B3%A0DB%20%EB%A9%80%ED%8B%B0%EC%86%8C%ED%8C%85%20Not%20Correct%20%EC%98%88%EC%A0%9C.png)
- 하나의 컬렉션을 여러 컬렉션으로 나누기
  - 하나의 컬렉션이 너무 많은 document를 가질 경우엔 index size가 증가하고 index cardinality가 낮아질 가능성이 높다
  - lookup performance 악영향을 미치고 slow query를 유발
  - 컬렉션을 여러 컬렉션으로 나눠 query processor가 중복되는 index를 look up하는 것을 방지
- Thread를 이용해 대량의 Document를 upsert
  - 여러 개의 Thread에서 bulk operation을 통해 한번에 write 진행
- Mongo DB 4.0 이후 버전 사용
  - ![몽고 DB 4.0.png](image%2F%EB%AA%BD%EA%B3%A0%20DB%204.0.png)
- key examined 값을 8000~9000을 넘어가면 100ms 이상 소요됨
  - 조건을 추가하여 8000아래로 떨어뜨리는 방식이 좋음

## Bulk insert 방법
- index는 write 성능 저하를 야기할 수 있기 때문에 많은 고려가 필요함
- bulk insert가 필요할 경우 100번에 나눠서 요청을 하는 것보다 100개를 한 번에 요청하는 게 빠르다
  - insertMany(), bulkWrite() 를 제공함

## Reference
- https://tv.naver.com/v/11267386