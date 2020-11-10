# Dmart 프로젝트

현실 세계의 도메인을 접목시켜서 새로운 기술을 학습하기 위한 프로젝트입니다.

## 목표

- MSA 에 대해 학습하고, 이를 적용시켜본다.
  - 서킷 브레이커를 적용시켜본다.
  - 분산 트랜잭션을 적용시켜본다.
- Spring Boot Application을 Dockerizing한다.
  - Kubernetes는 사용하지 않는다.
- Spring Data JPA를 활용한다.
- 백오피스도 만들어본다.

## 기간

2020.11.09 ~ 2020.12.04

일단 4주간 진행할 수 있는 만큼 진행을 한다.  
다른 일정도 있는 만큼 기술을 학습하는데에 집중한다.

## 무엇을 만들것인가?

기존에 만들었던 배민찬 프로젝트를 좀 더 발전시킨 형태로 만듭니다.

기존 프로젝트는 사용자에게 보여지는 화면에 출력되는 정보만 작업했는데, 백엔드 개발자에게 중요한 비즈니스 로직을 구현해보고 싶었습니다.

### 도메인

#### 포함하려고 하는 것

- 결제(고려해야할 것이 너무 많음 => 기술과는 관계없는 비즈니스가 많이 포함될 가능성이 있음)
- 정산(결제가 없더라도 정산시스템을 작성할 수는 있을 것 같다.)
- 주문(사용자 주문시 분산트랜잭션 구현)
- 재고
- 고객 관리
- 판매자 백오피스
- MD 백오피스
- 고객센터 백오피스
- 배송
- 반품, 교환

#### 분리

DB와 도메인이 독립적으로 있어야 할 것 같다.  
근데, 어떻게 나눠야 잘 나누는건지 잘 모르겠고, 경험이 없는 도메인을 무턱대고 나누려는 느낌이 굉장히 많이든다.  

##### DB

- 고객
- 상품
- 주문
- 배송
- ..?

##### 각각의 도메인

보통 DDD 스타일로 많이들 만드는 것 같다.

딱히 Best Practice라고 할만한 것이 없어서 한 번 목요일에 교보문고 가서 관련 서적을 읽어봐야겠다.
