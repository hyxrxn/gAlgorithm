### 25214 - 크림 파스타

## 문제 조건 분석
처음에 A_i 의 범위를 보고 O(n) 으로 해결해야 하는 줄 알고 고민을 좀 했다가 조건을 잘못 본 것을 알게 되었다.
N <= 2 * 10^5 이므로 O(n^2) 보다 작으면 해결되겠다고 생각했다.

## 오류
문제를 잘못 해석했다.
i <= j 라는 조건을 못봐서 배열을 앞에서부터 순회하며 최대값과 최소값을 갱신하고, 그 차를 출력했었다.
이는 앞선 조건이 포함되지 않은, 지금까지의 수열에서 순서에 상관없이 제일 큰 차를 반환하는 로직이어서 틀렸다.

## 정정
결국 뒤에 들어온 것에서 앞에 들어온 것과의 차이가 커야하므로 지금 들어온 값보다 먼저 들어온 값들에 의해 결정되는 것이다.
또한, 이전까지의 차의 최대값을 출력하는 것이므로 이전 출력값보다 작아질 수 없다.
이들에서 힌트를 얻었다.
하나씩 순회하면서 이전의 최소값과의 차이를 확인하였고, 이와 이전까지의 최대차를 비교하여 더 큰값을 저장하도록 했다.