# Portfolio-with-Python

파이썬으로 배우는 포트폴리오 도서를 읽고 정리한 레포지토리입니다.

<div>
</div>

## 기록

* 포트폴리오 효과 : 포트폴리오를 구성해서 같은 기대수익률 하에 위험이 줄어드는 것
* 두 자산의 움직임이 반대로 갈 때, 즉, 상관관계가 -1에 가까울수록 분산 효과가 큼

<div>
<br>
</div>

* 포트폴리오를 평가하는 지표
  
  * 샤프지수 : 위험 한 단위를 감수할 때 얻을 수 있는 초과수익. 수익이므로 높을수록 좋음
  
  * 젠센알파지수 : 포트폴리오 수익률과 기대수익률의 차이. 시장 대비 얼마나 높은 성과를 냈는지 알 수 있으므로 높을수록 성공적인 투자였음을 의미. 기대수익률은 펀드가 추종하는 벤치마크지수로 볼 수 있음
  
  * 트레이너지수 : 위험보상비율. 샤프지수와 다른점은 분모를 수익률의 표준편차(총위험의 척도)가 아닌 베타(시장위험의 척도)를 사용하는것. 이는 포트폴리오 분산이 잘 이루어졌다면 개별 종목에 대한 비체계적 위험은 없어지고 시장의 위험만 존재한다고 가정하기 때문임. 이 또한 높을수록 성과가 좋음을 의미
  
  * 정보비율 : 초과수익를 리스크로 나눈 값. 위험조정 후 수익률이 수익률의 변동 혹은 위험에 노출된 대가로 달성된 것인지를 파악함
  
  * 최대 낙폭(MDD) : 특정 기간에서 고점에서 저점까지의 최대 누적 손실. 고점에서 차기 저점까지의 하락폭이 가장 큰 구간의 등락률로, 기존의 표준편차가 놓치기 쉬운 하락위험을 잘 설명함

<div>
<br>
</div>

* 평균-분산 포트폴리오 이론
  * 위험을 줄이고 수익률을 높이기 위해 상관계수가 낮은 자산을 결합해 최적 포트폴리오를 구성할 수 있음
  * 포트폴리오의 기대수익률 : 수익률*기대값
  * 포트폴리오의 위험 : (주식 A 투자비중^2) * (주식 A 분산) + (주식 B 투자비중^2) * (주식 B 분산) + 2 * 주식 A 투자비중 * 주식 B 투자비중 * 포트폴리오 공분산

<div>
</div>

* 최소분산포트폴리오
  
  * ![최소분산포트폴리오](images/최소분산포트폴리오.jpg)
  
  * 가로축은 위험, 세로축은 이익
  
  * 상관계수가 -1일 때 포트폴리오가 만들어내는 조합의 좌표는 가장 윗쪽 직선상에 찍힘(optimal한 경우)
  
  * 상관계수가 1일 때 가장 아랫쪽 직선상에 찍임(worst)
  
  * 가능한 지점 중 위험도가 가장 낯아지는 부분이 최소분산포트폴리오 조합

<div>
</div>

* 포트폴리오 베타
  * 포트폴리오를 구성하는 자산의 수가 늘어날수록 리스크는 줄어들지만, 일정 수준 이하로는 내려가지 않음
  * 이처럼 제거할 수 없는, 시장 전체에 공통으로 미치는 체계적 위험(Systemic Risk)를 베타라고 함
  * 시장 수익률에 대한 민감도를 의미하며, 시장 수익률이 1% 변할 때 종목 수익률이 몇 % 변하는지 나타냄.
    * 베타가 1이면 시장과 같은 변동성을, 1보다 낮으면 시장에 둔감하게 움직임
  * 기대수익률과 마찬가지로 구성 자산 베타의 가중평균과 같음
  * 일반적으로 기술주의 베타는 1 이상이고, 경기방어주는 1 이하의 값을 가짐

<div>
</div>

* 샤프 비율 : 투자자가 부담하는 위험에 대해서 자산 수익률이 얼마나 잘 보상하는지에 대한 지표
  * 따라서 같은 기준지표로 두 자산을 비교하면, 높은 샤프 비율을 가진 자산이 더 효율적임
  * 최적의 포트폴리오는 샤프 비율이 가장 높은 포트폴리오로, 자본시장선과 효율적 포트폴리오 접선 위에 위치함

<div>
</div>

* 블랙-리터만 모델
  
  * 평균-분산 모델은 다수 자산에 투자 비중이 분배되지 않고 일부 자산에 과도하게 편중되는 경우가 잦음. 이는 기대수익률/위험 측정 오차가 최적화 단계에서 증폭되어 포트폴리오 투자 비중이 민감하게 반응하여 발생하는 현상
  * 블랙-리터만 모델은  베이즈 정리를 사용해 투자자의 견해를 고려하며, 자산을 시장가치에 비례해 투자함으로써 앞선 문제들을 해결했음

<div>
</div>

* 파마-프렌치 3요인 모델
  
  * 베타는 주가 결정력이 없으며, 단순히 하나의 위험지표만으로는 수익률을 설명할 수 없음
  
  * 파마-프렌치 3요인 모델은 시가총액, BR/ME(주가순자산비율(PBR)의 역수), 시장이라는 세 변수를 사용하며, 이를 통해 시가총액이 작고 PBR이 낮은 종목(가치주, 1 이하)일수록 초과수익을 올리기에 유리하다는것을 증명
  
  * CAPM을 기반으로 복수의 리스크-시장 리스크, 가치 리스크, 규모 리스크-를 고려함
  
  * 경험적으로 CAPM은 시장 변동성의 70%를 설명하고 파마-프렌치 3요인 모델은 90% 이상을 설명함

<div>

</div>

* 머신러닝
  
  * KNN으로 다음날 가격의 상, 하향을 예측한 결과 S&P 수익률에 미치지 못한 나쁜 결과가 나타남
  
  * 로지스틱 리그레션도 동일하게 사용한 결과, S&P를 상회하는 수익률을 보여줌
  
  * 설명변수에 따라 성능이 크게 차이남
