# Info
[창영이와 퇴근](https://www.acmicpc.net/problem/22116)

## 💡 풀이 방법 요약

A_(1,1) 에서 A_(N,N) 까지 경로에서의 경사의 최댓값을 해당 경로의 비용이라고 생각하면,

한 점 부터 다른 점까지의 최소 비용를 구하는 과정이므로 다익스트라를 생각했습니다.

시작점으로부터 상하좌우를 보면서 순회했고, 그 중 아직 방문하지 않은 점으로 경로를 이어갔습니다.

지금까지 계산된 경로 상의 최댓값과 이전 점과 지금 점 사이의 경사중 큰 값을 저장합니다.

따라서 저장한 값 중 도착점에서의 값이 바로 시작점에서부터 최소 비용이 됩니디.

## 👀 실패 이유

많이 실패했는데요,,,

처음에 다익스트라로 접근하니 시간 초과가 났고, 우, 하만 순회하도록 하니 틀렸습니다.

이후 방법을 바꿔 크루스칼 알고리즘을 차용해 최소 비용 간선부터 추가하면서 시작점과 도착점의 부모 노드가 같아지는 시점에 종료하도록 구현했는데,

union, find 의 시간복잡도가 작지 않아 또 시간 초과가 났습니다.

이후 다시 다익스트라로 돌아와 이것저것 바꿔보며 시간 초과를 보다가,

마지막에 들어 탐색하는 경우를 좌, 상 보다 우, 하를 먼저 보도록 하니 통과했습니다.

## 🙂 마무리

앞으로 진행 방향은 생각없이 정하지 않겠습니다.