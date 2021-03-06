# BFS 너비 우선 탐색

- Graph 자료구조를 순회하는 알고리즘
- 최단거리를 구하는 간단한 알고리즘
- 방문한 노드에서, 방문한 그 순간에 최단거리를 확정짓는 알고리즘이다.
- 모든 노드는 한 번만 방문한다.
- 한 노드를 방문하고, 모든 인접 노드를 방문한 후, 다음 노드로 향한다.

### logic

1. 나를 먼저 방문
2. 내 주변의 인접 노드들을 모두 방문한다. (확인한다는 개념이 더 이해가 잘 될듯)
3. 내 주변의 인접 노드들을 모두 확인하면서, 다음에 이동할 후보지에 넣는다.
4. 내 주변의 인접 노드들을 모두 확인했다면, 후보지에서 제일 처음에 있는 노드로 이동한다.

### So,

- 후보지를 저장할 Queue가 필요하다.
- FIFO구조로, 내 주변의 모든 가능한 경로를 확인하기 때문에, 이동 시점에 최단 경로가 확정된다.
- Queue에 entry Point를 삽입하고, BFS를 돌려야 한다.
- Queue를 알고리즘마다 구현하기 귀찮으니 STL 라이브러리를 사용하자.

### O(V+E)

- 모든 노드를 방문하는 것 O(V)
- 모든 노드에서, 인접 노드를 방문하므로 결국 O(E)가 된다.

따라서 시간복잡도는 O(V+E)다.
