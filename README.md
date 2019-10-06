# awesome-ml
docs

### Utils
- [Bayesian Optimization; hyperparameter?](http://research.sualab.com/introduction/practice/2019/02/19/bayesian-optimization-overview-1.html)

### Videos
- [Attention Models and Memory Networks](https://www.youtube.com/watch?v=JqkfT1s60cI&list=PLep-kTP3NkcOjOS1a30UNW-tH2FSoGYfg&index=2&t=0s)

### 용어정리
- L_p norm : (sigma(|x|^p))^(1/p) // 수식쓰는 방법 터득 후 수정하겠음.
- L_1 regularization : 가중치(w)가 너무 크지 않은 방향으로 학습. L1 Norm 은 파란색 선 대신 빨간색 선을 사용하여 특정 Feature 를 0으로 처리하는 것이 가능하다고 이해할 수 있다. 다시 말하자면 L1 Norm 은 Feature selection 이 가능하고 이런 특징이 L1 Regularization 에 동일하게 적용 될 수 있다.
  - regularized_cost = (1/n)*sigma(Loss(y_i,f(x_i))+(lambda/2)*|w|)
  - ![image-20191006170355464](/Users/jaejin/Library/Application Support/typora-user-images/image-20191006170355464.png)
  - ![image-20191006170412404](/Users/jaejin/Library/Application Support/typora-user-images/image-20191006170412404.png)
  - L1 regularization 을 보면, w 값이 업데이트 될때, 일정한 상수 값이 계속 빼진다. 즉, 작은 값들은 0으로 수렴하여 그 영향도가 무시된다.

- L_2 regularization : L1 과 마찬가지로, 가중치(w)가 너무 크지 않은 방향으로 학습.
  - regularized_cost = (1/n)*sigma(Loss(y_i,f(x_i))+(lambda/2)*|w|^2)
  - ![formula](https://chart.googleapis.com/chart?cht=tx&chl=C%20%3D%20C_0%20%2B%20%5Cfrac%7B%5Clambda%7D%7B2n%7D%20*%20%5Csum_w%7Bw%5E2%7D)
  - ![formula](https://chart.googleapis.com/chart?cht=tx&chl=%5Cfrac%7B%5Cpartial%7BC%7D%7D%7B%5Cpartial%7Bw%7D%7D%20%3D%20%5Cfrac%7B%5Cpartial%7BC_0%7D%7D%7B%5Cpartial%7Bw%7D%7D%2B%20%5Cfrac%7B%5Clambda%7D%7Bn%7D%20*%20w)
  - ![formula](https://chart.googleapis.com/chart?cht=tx&chl=w%20%5Crightarrow%20w%20-%20%5Ceta%20%5Cfrac%7B%5Cpartial%7BC%7D%7D%7B%5Cpartial%7Bw%7D%7D%20%3D%20w%20-%20%5Ceta%20%5B%5Cfrac%7B%5Cpartial%7BC_0%7D%7D%7B%5Cpartial%7Bw%7D%7D%20%2B%20%5Cfrac%7B%5Clambda%7D%7Bn%7Dw%5D)
  - L2 regularization 을 보면, w 에 1보다 작은값이 계속 곱해지는 걸 보아, 특정값이 너무 커지지 않게 방지한다.

### REFERENCE
1. https://light-tree.tistory.com/125
