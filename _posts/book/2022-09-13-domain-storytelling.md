---
layout: post
title: Domain Storytelling, A Collaborative, Visual, and Agile Way to Build Domain-Driven Software
description: >
  **디지털 전환(DX) 실현을 위한 기초 기술 ‘마이크로서비스’의 핵심을 쉽고 빠르게 습득하자!**
  이제는 마이크로서비스 방식으로 애플리케이션을 개발하고, 그 애플리케이션을 컨테이너에 배포해서 실행하며, 오케스트레이션 기능을 통해 컨테이너화된 애플리케이션을 운영한다. 이 책은 바로 이 마이크로서비스가 무엇인지, 애자일이 무엇인지, 클라우드가 무엇인지, 그리고 디지털 혁신이 무엇인지 등 마이크로서비스와 관련된 기술 요소를 폭넓게 다루면서 그 핵심을 한눈에 볼 수 있도록 그림과 함께 쉽게 설명한다.

tags: [book]
author: author2
canonical_url: https://jpub.tistory.com
---

[Domain Storytelling] (사진)
[Domain Storytelling] (출판사 책 설명 링크)

하단의 내용 목차형태로 넣는거 하기

# Part I: Domain Storytelling Explained
## Chapter 1: Introduction
### What Is Domain Storytelling?
- 정의: 도메인 스토리텔링이란 팀이 일하는 방식을 강조하는 협업을 통해 모델링하는 기술 목적: 서로 다른 배경/경험을 가진 사람들을 모아 서로 설명하고 시각화, 즉 도메인 지식을 비즈니스 소프트웨어로 변환하는 것 부가적으로 참여자의 이해의 깊이를 맞출 수 있음

- 스토리텔링은 각자의 경험을 바탕으로 설명하고 듣고 이해함으로써, 소프트웨어 개발에도 유용함

> - 도메인의 이해   
> - 도메인 전문가와 IT전문가 간의 공유 언어 구축   
> - 오해 해소(극복)   
> - 소프트웨어 요구사항 명확화   
> - 올바른 소프트웨어 구현   
> - 구축할 소프트웨어 구조화   
> - 실행 가능한 소프트웨어를 만들 수 있게 하는 비즈니스 프로세스 설계

중요한 것은 설명하기와 듣기 뿐 아니라 모두가 이해할 수 있는 언어(모델)로 시각화 하는 것임

### Your First Domain Story
*나중에 작성하기*


## Chapter 2: The Pictographic Language
> *"상호 의사소통이 가능한 수준으로 표현된 이미지/아이콘"*이라는 뜻으로 해석하는게 좋을 듯

### Actors
> 액터, 사용자, 역할자의 의미로 이해하면 될 듯

이미지

- 도메인 스토리는 Actor의 관점에서 전달된다.
- 의미를 명확하게 표현할 수 있는 아이콘을 그리고, 하단에 구체적인 역할의 이름을 작성한다. 일반적으로 명사형
- 이름은 구체적이고 명확한 도메인 언어로 표현한다. (예)"영화팬"은 영화티켓을 구매하기 위해 돈을 지불한다.
- Actor는 도메인 스토리에 한번 출현(?)한다. 아래 설명할 Work Objects는 어려번 나타날 수 있다.

### Work Objects
> "작업 객체, 객체 자체 또는 작업 객체에 대한 정보가 교환되는 매체"

이미지

- 의미를 명확하게 표현할 수 있는 아이콘을 그리고, 하단에 구체적인 객체의 이름을 작성한다. 일반적으로 명사형
- 도메인의 개념은 Actors와 Work Objects로 모델링 될 수 있다. 따라서 다른 어떤 유형보다도 이 두개의 유형울 **심플하지만 명확하게 표현**하는것이 중요하다.
- 아이콘은 Google의 Matrial 아이콘을 사용한다. 아이콘은 표현하려는 정보의 의미를 명확하고 단순하게 표현할 수 있는 것을 선택한다. 너무 많은 아이콘들을 사용하면 이해하 어려울 수 있다. (작성한 사람도 며칠 후 다시보면 이해 안갈 수 있음)

### Activities
> 활동, Actors의 행위 또는 활동

이미지

- 행위자의 활동을 방향이 있는 화살표로 표시하고 하단에 활동 내용을 작성한다. 일반적으로 동사형

### Sequence Numbers
> 일련번호, 스토리들의 순서를 나타내는 숫자

이미지

- 스토리는 어려개의 문장으로 표현되므로 일련의 순서를 원 안에 숫자를 기입해서 부여한다.
- 일반적으로 Activities(활동)을 나타내는 화살표 상단에 숫자를 작성한다.
- 대부분의 활동이 연속적으로 발생하므로 숫자는 보통 한번 만 사용되지만, 동시에 발생하는 활동의 경우 동일한 번호로 작성할 수 있다. *단. 활동 순서 이해가 어려워질 수 있으므로 가능한 적게 사용하는 것을 추천*

### Annotations
> 주석, 구성요소 등 모델에 대한 부연설명

이미지

- 모델링 공간의 빈곳, 여백에 주석을 작성하고 부연 설명하려는 항목에 점선으로 연결한다.
- 아이콘과 이름으로 이해하기 어려운 부분, 부가적인 설명이 필요한 부분이 있는 경우 작성한다.
- 별도 작성 방법이나 템플릿은 없지만, 명확하게 이해될 수 있도록 작성하는 것이 중요하다.

### Modeling Canvas
> 모델링 캔버스, 화이트 보드 등 모델링 할 공간으로 아날로그, 디지탈 다 가능 (제한없음)

이미지 

- 캔버스에 도메인 스토리 이름을 작성한다.
- 도메인 스토리가 동작하기 위해 필요한 Assumtions(기정/추정)을 작성한다. (Optional)
- 도메인 스토리의 Activities를 설명하는 Comments를 작성한다. (Optional)
### Groups
> 그룹, 스토리 내 묶을 수 있는 하위 스토리의 묶음

이미지 

- 스토리 내에 함께 묶을 수 있는 스토리들을 묶는다. 직사각형, 원 또는 모든 형태로 표현할 수 있다.
- 그룹 이르을 작성하고, 그룹의 의미를 설명할 수 있는 내용을 작성한다.
- 그룹으로 표현할 수 있는 몇가지 예시
  - 반복되는 활동
  - 선택사항(Optional)인 활동
  - 다른 곳에서 일어나는 스토리
  - 조직의 경계
  - 하위 도메인(?)

  하위도메인 이미지

### Colors
> 색상, 강조 또는 차별화를 표현하기 위해 아이콘/이름에 검정색 외 다른 색상으로 표시

이미지

- 일반적으로 도메인 스토리 모델은 검정색, 즉 흑백으로 표현하지만, 강조 또는 차이점을 시각화하기 위해새 색상으 추가할 수 있다.
- 색상은 Actors, Activities 등 모든 유형에 적용할 수 있다.
- 색상은 어떤 모델링 도구를 사용하는지에 따라 사용할 색상이 결정될 수 있고, 이때는 색상의 의미를 나타내는 범례를 추가하는 것이 좋다.

예시 이미지

### No Conditionals
BPMN, Business Process Model and Notation과 비슷한데 분기/조건 부분을 단순화한 형태 사용 이유, 목적에 대해서 좀더 알아보고 업데이트 예정임


### Putting It All Together


### A Grammar for Domain Stories Good Language Style


## Chapter 3: Scenario-Based Modeling (시나리오 기반 모델링)
> *"도메인 스토리"*란,   
사람들 사이의 목표가 있는 행위를 Activities와 Event로 구성   
따라서, 시나리오 기반 모델링이란, 사람들 사이의 목표가 있는 행위를 누구나 이해할 수 있는 Actors, Work Objects, Ativities 등을 심플한 아이콘과 레이블로 표현한 것이다.

- What Are Scenarios?
  - 사람들과 그들의 활동에 대한 이야기
  - 목표가 있는 행위자가 포함
  - 줄거리가 있고 이것은 일련의 활동과 이벤트로 구성됨

  > 즉, 도메인 스토리는 시나리오다.

- Scenarios in Domain Storytelling
  - 80% 수준의 기본 사례와 Happy Path를 먼저 모델링하는 것이 좋다. 이는 프로세스의 목적에 대한 일반적인 아이디어를 제공, 목적을 이해하는 데 도움이 된다.
  - 먼저 일반적인 사례에 대해 이해한다, 즉 이야기를 하고, 그 이후 규칙을 찾아 다른 일이 발생할 수 있는지 논의한다.  

- Concrete Examples as Scenarios
  - 일반적인 사례, Happy Path로도 시나리오 식별이 어려운 경우, 과거의 실제 사례의 몇가지 예를 모델링하는 것이 도움이 될 수 있다.

- Keeping an Overview
  - 완성도가 아닌 대표 표본에 집중한다.
  - 복잡한 비즈니스를 모델링해야하고, 중요한 변형(분기, 예외 등)이 있는 경우 많은 도메인 스토리가 만들어야 하는 경우, 전체 스토리를 다 모델링하지 않고 비즈니스 프로세스의 가장 중요한 시나리오를 모델링해서 초기 개요(Overview)를 유지, 잊지 않는 것이 중요하다.

## Chapter 4: Scope (범위)
> 도메인 스토리텔링은 스토리를 어느수준으로 상세히 설명할 것인지, 어느 범위를 설명할 것인지 정의해야 한다.

### Granularity
상위 수준의 도메인 스토리를 상세한 하위 수준의 도메인 스토리로 모델링한다.   
아래 그림은 영화 관람객이 매표소에서 티켓을 구매하는 방법, 스토리를 상세하게 모델링 한 것이다.

이미지

그림과 같이 스토리는 세분화의 수준에 따라 다르다. 표현하려는 스토리에 맞게 수준을 정해서 모델링 하는 것이 중요하다. 즉 목적에 맞는 모델링이 필요하다.

[ 스토리텔링 표현 수준 ]
> - Cloud Level
> - Kite Level
> - Sea Level : 보통 이 레벨에서 스토리텔링 모델링을 시작하며, 필요에 따라 상위 또는 하위 레벨 모델링한다.
> - Fish Level
> - Clam Level

### Point in Time (AS-IS vs. TO-BE)
모델링의 목적은 잘못된 것을 개선하거나, 문제를 해결하는 것이기 때문에 현재 상황을 문제영역으로 정한다. 또한 도메인 스토리를 통해 개선 방향이나 개선 방법을 탐색해서 솔루션 영역에 모델링 할 수도 있다.

이미지

- AS-IS 스토리 : 이렇게 현재 상황을 문제영역으로 정하고 모델링하는 것, 현재 상황 == 문제 영역
- TO-BE 스토리 : 개선 방향이나 방법을 솔루션 영역에 모델링하는 것, 개선된 상황 == 솔루션 영역

### Domain Purity (PURE vs. DIGITALIZED)
도메인 스토리를 모델링할 때 As-is 또는 To-be 소프트웨어 시스템을 포함하거나 생략할 수 있다 이 범위를 도메인 순도(Domain Purity)라고 한다.

- 순수 (Pure, 소프트웨어 시스템이 없는 도메인 스토리) : 신규 소프트웨어 시스템을 구축할 때 유용 (기존 소프트웨어에 기능 추가로 인한 복잡성을 소프트웨어적으로 모델링하지 않음으로 복잡성을 낮출 수 있다.)
- 디지털화 (Digitalized, 소프트웨어 시스템이 있는 스토리

> 개인적으로는 As-is 시스템을 도메인 스토리로 시각화하고, To-be 시스템을 순수 도메인 스토리로 모델링, 이후 소프트웨어 시스템으로 구현할 것들을 디지털화 모델링하는 것이 좋은 방법이라고 생각함

### Combining the Scope Factors: A Typical Journey
범위는 여러 요소를 결합해서 정할 수 있다.

> Scope = Granularity X DomainPurity X PointInTime
>
> *"굳이 공식까지 만들 필요가 있을까 싶다..."*

[ 도메인 스토리의 일반적인 여정 ]

- 새 도메인 탐색 : 거칠고 순수한, As-is 모델링 (Coase-Grained, Pure, As-is)
- 하위 도메인으로 드릴다운 : 세밀하고 순수한 As-is 모델링 (Fine-Grained, Pure, As-is)
- 새로운 소프트웨어 소개 : 세밀하고 디지털화된 To-be 모델링 (Fine-Grained, Digitalized, To-be) 글자 그래도 일반적인 여정이니 상황에 맞게 자유롭게 범위를 정해 모델링하면 된다.

**[ 다양한 목적을 위한 스토리텔링과 범위 조정의 예 ]**

- **새로운 도메인 탐색 (Coase-Grained, Pure, As-is)**   
  순수한 도메인 자체를 이해하기 위해서는 소프트웨어 시스템을 생략하고, 고객의 관점에서 목적을 바라보면서 모델링하는 것이 좋다. 따라서 도메인 스토리는 종종 종단간 비즈니스 프로세스를 표현한다.

  도메인 영역 탐색을 시작할 때, 도메인 스토리의 개요를 모델링할 때, 도메인 영역에서 경계를 찾으려 할 때 이 방법을 사용할 수 있다. 순수한 도메인 자체를 이해하기 위해서는 소프트웨어 시스템을 생략하고, 고객의 관점에서 목적을 바라보면서 모델링하는 것이 좋다. 따라서 도메인 스토리는 종종 종단간 비즈니스 프로세스를 표현한다.

- **하위 도메인으로 드릴다운 (Fine-Grained, Pure, As-is)**   
  도메인을 빠르게 참색하고 프로젝트 범위에 대한 컨센서스를 맞췄다면, 이후 상세하게 드릴 다운한다. 앞에서 도메인 전체를 조망했으니, 이번 단계에서는 하위 도메인에 집중해서 모델링한다. 하위 도메인은 보통 한 부서 내에서 발생하는 스토리 수준으로 정한다.

  다른 하위 도메인 간, 부서 간의 인터페이스를 볼 수 있도록 하위 도메인의 시작과 끝에 커멘트(추가 설명)를 작성하면 좋다. 이렇게 하면 부서의 경계를 넘어 함께 일하는 방식을 이해하는데 도움이 된다.

  이 방법을 통해 개선된 소프트웨어의 지원으로 해택을 얻을 수 있는 비즈니스 프로세스를 찾을 수 있으며, 기술적으로 복잡하지 않은 순수한 도메인 모델을 추출하고 모델을 구현할 수 있다. 또한 As-is와 To-be 도메인 스토리를 비교해서 작업(프로세스)가 어떻게 변경되는지 시각화할 수 있다.

- **신규 소프트웨어 도입(Fine-Grained, Digitalized, As-is)**   
  As-is에 개선된 프로세스, 새로운 역할, 새로운 소프트웨어가 어떻게 추가/변경되는지 표현한다. 세밀하고 디지털화된 To-be 스토리는 미래에 사람(역할자)과 소프트웨어 시스템이 함께 작동하는지를 보여준다. 즉, 이번 단계에서는 개선사항이 소프트웨어로 구현되었을 때 기존의 작업(프로세스)가 어떻게 변경되는지를 시각화한다.

## Chapter 5: Modeling Tools (모델링 도구)
- Modeling on Paper or Boards
- Modeling with Software Tools
- Choosing a Tool
## Chapter 6: The Workshop Format
- Before the Workshop
- The Workshop
- After the Workshop
- TO-BE Workshops
- Remote Workshops
- The Moderator
- The Modeler as Separate Role
- Moderated Mode vs. Co-Op Mode
## Chapter 7: Relationship to Other Modeling Methods
- Domain-Driven Design
- EventStorming
- User Story Mapping
- Example Mapping
- Storystorming
- Use Cases
- UML
- BPMN
- Summary
# Part II: Using and Adapting Domain Storytelling for Different Purposes
## Chapter 8: Case Study—Alphorn Auto Leasing Inc.
- Explore Alphorn—The Domain as a Whole
- Drill Down into Risk Assessment—Understanding an Important Subdomain
- Clear Up Risk Assessment—Avoid Technical Jargon
- Optimize Risk Assessment—The TO-BE Process
- Introduce New Software—Combine Business Processes with IT Support
- Summary
## Chapter 9: Learning Domain Language
- Speaking and Listening to Understand Each Other
- Organizations Speak Many Domain Languages
- Using Natural Languages
- Lost in Translation
- What to Read Next?
## Chapter 10: Finding Boundaries
- The Joy of Multiple Models
- A Heuristic for Finding Subdomains
- From Subdomains to Bounded Contexts
- From Context Boundaries to Team Boundaries
- What to Read Next?
## Chapter 11: Working with Requirements
- Software Development as a Series of Conversations
- From Domain Stories to Requirements
- Adapt the Recipe
- Limitations
- What to Read Next?
## Chapter 12: Modeling in Code
- From Domain Stories to Domain Model
- Implementing the Domain Model
- What to Read Next?
## Chapter 13: Supporting Organizational Change
- Changing People’s Workflows
- Digitalizing Work
- What to Read Next?
## Chapter 14: Deciding Make or Buy and Choosing Off-the-Shelf Software
- Understand the Processes of Off-the-Shelf Solutions
- What to Read Next?
## Chapter 15: Finding Shadow IT
- Not Only Software Developers Develop Software
- Making Hidden Software Systems Visible
- What to Read Next?
## Chapter 16: Conclusion
- The Future of Domain Storytelling
- The Essence of Domain Storytelling
# Appendix: The History of Domain Storytelling
# Glossary
# Bibliography

