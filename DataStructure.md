# DataStructure

## Array vs LinkedList
### Array

- 배열이라고 하며, 데이터가 순서대로 저장이 되는 형태메모리의 위치가 고정적이고 연속적인 형태
- **Memmory Area** : Heap Area
- **Insertion, Deletion** : 메모리의 위치가 고정적이고 연속적인 형태이기 때문에 저장, 삭제 시 메모리 재할당과 메모리 위치 변경의 시간이 많이 소요
- **Search** : index를 갖고 메모리에 접근하여 O(1)의 탐색이 가능

### LinkedList

- 리스트라고 하며, 데이터가 앞과 뒤 노드와의 연결성을 갖고 저장이 되는 형태
- 메모리의 위치가 동적이며, 연속적이지 않은 형태
- **Memmory Area** : Heap Area
- **Insertion, Deletion** : 메모리의 위치가 불연속적이고 가변적인 형태이기 때문에 저장, 삭제 시 삽입 삭제할 위치의 노드와 연결 혹은 연결 끊음만 해주면 되서 시간 소요가 적음
- **Search** : 이전, 이후 노드와의 연결을 보고 데이터를 찾아야 하기 때문에 순차적인 탐색이 이루어져 데이터 탐색 시간은 O(n)이 소요됨
- 흥미있는 Reference(LinkedList는 왜 Stack Memory에 할당되지 않을까?)
https://www.geeksforgeeks.org/why-linked-list-is-implemented-on-heap-memory-rather-than-stack-memory/

