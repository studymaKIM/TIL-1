## 개요
- 아침 TDD 스터디([프로젝트 리포지토리](https://github.com/pro00er/proMorningReader))와 clean Code 강의때 쓰인 가이드 pdf 를 실습하면서 유의미하게 느낀 것을 적음 
- [클린코드를 위한 TDD, 리팩토링 with Java](https://codesquad.kr/page/specialTdd.html?fbclid=IwAR0ajBv84g26Nv5sh1Zwwgj4Dmhs7HcQSvpjdr0s4EcT30Bekqsn8o3sjhI)

## Check
- 요구사항 분석을 통해 도메인 설계를 하라 (2019/01/09, 2019/01/10)
  - 한계를 느꼈던 건, ‘TDD 할때 테스트 케이스로 커버 안되는 구현,설계들은 어떻게 할까’ TDD 할때 요구사항 분석에서 바로 테스트 케이스 추출로 넘어갔음. 객체 추출, 도메인 설계를 의식적으로 하지 않음. 
  - 클린코드 강의 실습 가이드를 보고 갑자기 확 깨달음  
  - 오늘 pdf 다시 보고 느낌
  - > 요구사항 분석을 통해 대략적인 설계 - 객체 추출
    > UI, DB 등과 의존관계를 가지지 않는 핵심 도메인 영역을 설계
  - (2019/01/10) 요구사항보고 객체 설계부터 함. 객체 설계와 도메인 설계의 차이가 뭘까? 
    - (from 위키백과)도메인 : 문제를 풀기위해 설계된 어떤 소프트웨어 프로그램에 대한 기능성을 정의하는 연구의 한 영역 
    - 도메인 설계는 그럼 문제를 풀기위해 모델링 하는 건가? 음... DDD에서 정의하는 Domain에 대해서 더 알아봐야겠다. 
    - [ ] DDD 참고 리스트 읽기 ../concept/DDD.md
  - 이걸 의식적으로 하면 이 설계를 가지고 다중언어로 구현하는게 더 쉽지 않을까 하는 생각이 듦.   
    - python과 java를 오가면서 구현하면 언어특성에 대한 코드조각보다 설계를 더 보게 되는 것처럼(pythonic한 코드를 짜기에는 언어의 이해가 부족하니까...).
- 도메인 설계할때 '객체의 상태(속성)보다는 행위에 집중한다' 하는 이유가 뭘까? 가이드 PDF에서 아래 부분이 아직 와닿지 않음. 중요한 거 같은 감이 오는데 정확한 이유를 생각해서 말할 수가 없음

- 도메인 설계할때 사용할 기본적인 ClassDiagram 을 익혀야겠다. UML 책([UML 실전에서는 이것만 쓴다](http://www.insightbook.co.kr/book/programming-insight/uml-%EC%8B%A4%EC%A0%84%EC%97%90%EC%84%9C%EB%8A%94-%EC%9D%B4%EA%B2%83%EB%A7%8C-%EC%93%B4%EB%8B%A4)) 다시 읽어봐야겠다. UML툴을 따로 사용하지 않으니 오히려 UML이 '몇 가지 기호를 사용해 설계에 대해 모두가 알아볼 수 있도록 정한 약속'인 부분이 와 닿는다. 내가 UML을 알고 있어야 다음에도 내가, 다른 사람이 알아볼 수 있게 CD를 그릴 수 있잖아! 손으로 그리던지 마인드맵 어플을 사용하던지 상관없이 말이야.
- 기본 MVC Pattern 왜 이렇게 아직도 이해 못하는 기분이지. 설계할때 바로 MVC 가 그려지지 않는다. class 를 나눈다! 의 개념보다 어느 부분이 controller인지 파악하는 것이 좀 잘 안됨. 

- 핵심이 되는 작은 부분부터 개발하면서 서서히 덧붙여나가는게 TDD 구현순서 정할때 좋다
  - Fact : 한 번에 주어진 레이싱카 게임 요구사항을 구현하는 것보다 여러 버전으로 나누어서 구현한게 더 빠르고 쉽게 구현. 구현할때  좀 더 안정감 있었음(Feeling). 
  - Finding: 김창준 애자일 코치 칼럼([당신이 제자리 걸음인 이유 : 지루하거나 불안하거나](http://egloos.zum.com/agile/v/5749946) - b1. 난이도 낮추기 부분 참고 / [지금 하는 일들을 절반의 시간 안에 해야 한다면?](http://agile.egloos.com/m/5838463) )에서 읽은 적이 있다. 처음 불확실성이 높을 때 일을 쪼개서 내가 쉽게 할 수 있는 버전 1을 만들고 버전 2에서는 조금 더 복잡한 기능을 덧붙여 만들면서 버전을 업그레이드 해가면서 만들면 한번에 어려운 걸 구현하는 것보다 같은 시간 안에 더 빨리 안정감을 느끼면서 만들게 된다.

- 지금 사용하고 있는 Junit 테스트 프레임워크의 best sample이 궁금해짐
  - 전에 테스트를 접했을때 <<JUnit in Action>> 책을 읽다가 신나서 이것저것 적용해보고 결국엔 아, 내가 test가 아니라 JUnit을 하고 있구나를 깨달은 적이 있다. 아직 JUnit 설계를 보기보다 일단 tool로서 툴답게 사용하는 것에 집중하자. 때가 아니다.
  - 참고 article
    - [Junit - basic template](http://junit.sourceforge.net/doc/faq/faq.htm#tests_16) 
    - [testing-debugging/junit-best-practices - javaworld](https://www..com/article/2076265/testing-debugging/junit-best-practices.html)
    - [junit-best-practices - kyleblaney](http://www.kyleblaney.com/junit-best-practices/)

