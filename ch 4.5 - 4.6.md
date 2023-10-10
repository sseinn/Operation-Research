# ch 4.5 - 4.6

# Tie for the Entering Basic Variable / Entering Basic Variable의 동등한 해결 상태

각 반복의 단계 1은 현재의 방정식(0)에서 가장 큰 절댓값의 음의 계수를 가진 nonbasic variable를 entering basic variable로 결정한다.
만일 가장 큰(절댓값 관점에서) 음의 계수를 갖는다는 측면에서 2개 이상의 nonbasic variable가 동일한 값을 가진다고 가정하자.

예를 들어 Z = 3x1 + 3x2으로 변경된다면, 초기 방정식 (0)가 Z - 3x1 - 3x2 = 0이므로 첫 번째 반복에서 이러한 사태가 발생한다. 이와 동일한 상태는 어떻게 해결이 가능할까?

답은 이들 경쟁자들 중 임의의 하나를 선택하는 것이다. 
동일한 계수를 갖는 변수 중 어느 것을 선택하여도 궁국적으로 최적해에 도달할 것이며, 어떤 선택이 더 빨리 최적해에 도달하게 될지에 대한 사전에 아는 편리한 방법은 없다. 

이 예제에서는 x1을 inital enterinb basic variable로 선택하면 3번의 반복 후에 최적해 (2,6)에 도달하고, x2를 선택하면 2번의 반복 후에 도달한다.

# Tie for the Leaving Basic Variable - Degenearcy

이번에는 어떤 반복의 단계 2 에서 2개 이상의 basic variable이 leaving basic variable가 되기 위한 조건에서 동등한 상태라고 가정하자.

이런 상황이 발생하는 경우는 다음과 같이 일련의 사건이 발생 가능하므로 이론적으로 매우 중요하다. 

먼저 entering basic variable 값이 증가함에 따라 동일한 기준을 갖던 모든 basic variable들의 값이 동시에 0으로 떨어지다.
그러므로 leaving basic variable로 선택된 변수이든 선택되지 않은 변수이든 모두 새로운 BF solution에서는 0값을 값는다
 (basic variable인데 0값을 갖는 basic variable은 basic variable의  degenerate(퇴화)라고 불리며, 관련된 BF solution도 퇴화라고 부른다.)

두 번째로 degenerate basic variable는 계속되는 반복에서 degenerate leaving basic variable로 선택될 때까지는 0값을 가지고 있을 것이며 
(왜냐하면 그 변수는 degenerate leaving basic variable가 음수 값을 가지게 하지 않고서는 증가할 수 없기 때문이다),
 이는 Z값도 변화가 없을 것이다. 

세 번쨰로 Z가 매 반복에서 증가하지 않고 같은 값을 가지고 있다면, 심플렉스 방법은 최적해를 향해 언젠가 Z값이 증가하는 것 대신, 순환구조 (똑같은 해의 연쇄 구조를 주기적으로 반복하는 구조)를 갖게 될 수도 있다 .
 실제로 인위적으로 만들어진 예제들은 알고리즘이 퇴화의 덫에 빠져 영원한 순환구조(perpetual loop)를 돌 수 있음을 보여준다. 

 # No Leaving Basic Variable - Unbounded Z / Leaving Basic Variable이 없을 때 - 무한의 Z

어떤 반복의 단계 2에서 우리가 아직 다루지 않은 또 하나의 결과, 어떤 변수도 퇴출 기저변수로 선택할 조건을 만족시키지 못하는 경우가 있을 수 있다.
 이러한 결과는 현재의 다른 basic variable을 음수로 만드는 것이 없이 entering basic variable를 무한대로 크게 할 수 있음을 의미한다. 
 심플렉스 방법의 표 형식에서는 이것은 피봇 열의(행 0을 제외하고) 모든 계수가 음수이거나 0인 것을 의미한다.

 
![image](https://github.com/sseinn/Operation-Research/assets/143159192/de897c8e-7d4c-45be-a3d5-ab60ad78d851)

표 4.9에서 보인 것과 같은 표에 대한 해석은 제약식들이 objective function Z가 무한대로 증가할 수 있고, 심플렉스 방법은 Z가 무한대라는 메세지와 함꼐 정지한다. 

# Multiple Optimal Solutions / 복수의 최적해

최적해아 (2,6)과 (4, 3) 사이의 선분 위의 모든 점이 최적해가 될 수 있다. 
모든 최적해는 이러한 2개의 최적 CPF solution를 **가중 평균**한 하나의 점으로 나타낼 수 있다.

심플렉스 방법은 하나의 최적 BF solution을 찾으면 자동으로 정지한다. 
그러나 선형계획의 많은 응용들에서, 모형에 통합되지는 않았지만 복수의 최적해들 사이에서 의미있는 최적해의 선택을 가능하게 하는 무형의 요소들이 있다. 
이런 경우 이들 서로 다른 최적해들은 식별되어야 할 것이다.
앞서 언급한 대로 이는 모든 다른 최적해를 찾는 것을 요구하며, 모든 최적해는 최적 BF 해의 볼록집합니다. 
