---
layout: post
title: Beyond the Twelve-Factor App
description: >
  초기 Cloud 초창기에 경험 없는 기업이나 개발자가 새로운 Cloud 환경에 적합한 Application을 구축하는데 참고할 지침이었던 **12 Factor**.

  **Beyond the Twelve-Factor App: Exploring the DNA of High Scalable, Resilient Cloud Applications**은 원래의 12 Factor를 기반으로 현재까지의 모범 사례를 반영하고 또 우선순위를 부여하였다.
  
tags: [book]
author: author2
canonical_url: https://jpub.tistory.com
---

[Beyond the Twelve-Factor App] (사진)
[Beyond the Twelve-Factor App - Pivotal] (출판사 책 설명 링크)

# Preface (머리말)
이 책은 Cloud에 시스템을 구축하고 운영할때 참고할 수 있는 **The Twelve-Factor App**을 넘어 빠르게 변화하는 애플리케이션의 구축을 위한 현재의 문제를 해결하는 것을 목적으로 한다. 

- 설정 자동화를 위한 절차(declarative) 를 체계화 하여 새로운 개발자가 프로젝트에 참여하는데 드는 시간과 비용을 최소화한다.
- OS에 따라 달라지는 부분을 명확히하고, 실행 환경 사이의 이식성을 극대화 한다.
- 최근 등장한 클라우드 플랫폼 배포에 적합하고, 서버와 시스템의 관리가 필요없게 된다.
- 개발 환경과 운영 환경의 차이를 최소화하고 민첩성을 극대화하기 위해 지속적인 배포가 가능하다.
- 툴, 아키텍처, 개발 방식을 크게 바꾸지 않고 확장(scale up) 할 수 있다.

기업은 클라우드를 활용해 애플리케이션을 구축하면 비즈니스 변화에 시스템을 빨리 개선할 수 있고, 비용도 적게 드는 등 모든 것이 잘 될 것이라는 막연한 기대를 갖고 클라우드를 도입하고 있다. 그러나 대부분의 기업과 개발자는 Cloud에 친화적인 애플리케이션을 구축하는 방법을 잘 모른 채 시스템을 구축하고 있는게 현실이다.
이런 문제를 해결하기 위해 **"Heroku"**에서 **"Original 12 Factors"**를 통해 Cloud 도입 초기에 경험이 없는 기업, 개발자에게 Cloud에 Application을 구축하기 위한 방법을 제시하고 있다. 

Heroku는 12 Factors 개발에 "Pattern of Enterprise Application Architecture", "Refactoring"에서 영감을 받았다고 한다.

나도 이 두 책을 읽었지만 아무 영감도 못받았었음...

### 먼저, 12 Factors에 대해 알아보자.
1. Codebase : One codebase tracked in revision control, many deploys
2. Dependencies : Explicitly declare and isolate dependencies
3. Configuration : Store configuration in the environment
4. Backing Services : Treat backing services as attached resources
5. Build, release, run : Strictly separate build and run stages
6. Processes : Execute the app as one or more stateless processes
7. Port binding : Export services via port binding
8. Concurrency : Scale out via the process model
9. Disposability : Maximize robustness with fast startup and graceful shutdown
10. Dev/prod parity : Keep development, staging, and production as similar as possible
11. Logs : Treat logs as event streams
12. Admin processes : Run admin/management tasks as one-off processes

Original 12 Factors에 최신 지침을 추가한 Beyond 12 Factors도 알아보자.

# Beyond 12 Factors
## 1. One Codebase, One Application

> Cloud Native Application은 항상 버전 관리 시스템에서 추적/관리되는 단일 코드 베이스로 구성해야 한다.

하나의 Monolith 구조의 애플리케이션을 여러개의 Code Repository로 구성하는 경우, 애플리케이션의 빌드/배포를 자동화할 수 없다. 아얘 불가능하다.

하나의 애플리케이션을 관리하는 Code Repository 내에 별도 작업자가 있는 경우, 동일한 Code Repository의 Root를 공유하더라도 내부의 단일 애플리케이션을 위한 별도 Codebase가 있게 된다.

반대로 하나의 Codebase에 여러개의 애플리케이션을 관리하는 경우, 여러 팀에서 단일 Codebase를 관리하고 있다는 것을 의미하며, 버전관리에 여러움이 있을 수 있다. 내가 담당하는 모듈의 변경이 없었는데, 다른 영역의 변경에 따라 버전이 같이 올라가게 되는 문제 등이 있을 수 있다.
하나의 Codebase에 여러개의 애플리케이션을 관리할 수는 있지만 그건 공유코드가 아니라 각각이 Codebase라는 것을 의미한다.

당연한 얘기지만, 코드가 마이크로서비스여야 한다는 의미는 아니다.

## 2. API First
> 기존 12 Factors에는 없던 항목으로, 개발중인 애플리케이션의 유형과 상관없이 Cloud에 배포를 목적으로 애플리케이션을 구축하는 경우, 해당 시스템을 Cloud 환경의 에코 시스템에 참여시키는 것을 의미한다.

### - Why API First?
클라우드 환경의 에코시스템 내에 하나의 서비스로 구축/운영되려면 API라는 규정을 준수해야 한다. API가 곧 해당 서비스에서 제공하는 기능이므로, API를 구현을 목표로 개발하는 API First 방식을 따르는 것도 좋다.

### - Building Services API First
클라우드 내의 각 애플리케이션의 기능은 API를 통해 충족된다. 웹이든 모바일이든 사용자 인터페이스도 실제로는 API의 소비자라고 할 수 있다. (소비자: API를 호출해서 원하는 결과를 얻어가는...)
따라서, API를 먼저 설계하면 코드 구현 전에 이해관계자(내부 팀, 고객, API를 사용하려는 조직이나 팀)와 논의하기가 용이하다. 이 논의를 통해 User Story를 만들고 API를 모의하고, 사전에 테스트 문서도 생성할 수 있다. 즉 API를 통해 해당 애플리케이션의 기능/연동을 명확히 정의함으로써 명확한 개발과 연동을 사전에 검증하고 개발할 수 있다는 장점이 있다는 것이다.

## 3. Dependency Management (의존성 관리)
> 원래 12 Factors의 두번째 요소로 응용프로그램의 종속성의 관리방법, 위치 및 시기를 관리한다.

### Reliance on the Mommy Server
Mommy Server.. 엄마 서버로 해석하는게 맞는지 잘 모르겠지만, 뒤에 반대말이 단일 빌드 아티펙트... 라는 걸 보니 엄마보다는 애플리케이션의 모든 정보를 다 갖고 있는 서버의 의미로 해석하는게 좋을 것 같다.
즉, 기존 엔터프라이즈 환경에서는 애플리케이션이 필요한 모든 것을 제공하고, 의존성 관리부터 호스팅할 서버 정의한 것까지 애플리케이션의 모든 요구사항을 Mommy Server에서 처리했었다는 내용이다.

### Modern Dependency Management
모던, 즉 현대의 의존성 관리는 Java 언어의 경우 maven, gradle이 대표적이다. 
Cloud Native Application은 시스템 전체의 의존성을 한번에 관리하지 않고(할수도 없다), 애플리케이션 별로 의존성을 적적하게 관리하는 것이 애플리케이션별로 개선/배포에 적합하다.
각 애플리케이션(==마이크로서비스)별로 요구에 따라 의존성을 관리해야 한다라는 내용이다.
## 4. Design, Build, Release, Run
> 원래 12 Factors의 다섯번째 요소로 Build, Release, Run의 각 단계는 명확하게 분리해야 한다.
설계/개발/배포/실행의 전 과정을 CI/CD Pipeline을 통해 구성하며, 각 단계는 격리되어 개별적으로 동작/실행해야 한다. 
### Design
개발자는 애플리케이션의 의존성을 가장 잘 이해하고 있으므로, 설계단계에서 의존성을 선언/정의하고 애플리케이션과 함께 제공하거나 번들로 제공될 수 있도록 해야한다.
### Build
빌드 단계는 Code Repository가 바이너리 아티펙트로 변환되는 단계... 쉽게 말하면, Code가 배포/실행 가능한 형태로 만드는 단계란 뜻이다.
### Release
클라우드 환경이라면 빌드된 애플리케이션을 클라우드 환경으로 Push하는 것이다. 이때 애플리케이션과 애플리케이션 실행을 위한 환경정보, 구성정보가 통합된다. 
### Run
일반적으로 애플리케이션이 컨테이너(Docker, Garden, Warden 등)에 배치되고 프로세스가 시작되어 애플리케이션이 실행된다.

목표는 자동화된 테스트 및 배포를 통해 높은 신뢰도를 유지하면서 배포까지의 속도를 높이는데 있다.
## 5. Configuration, Credentials, and Code (구성, 자격증명, 그리고 코드)
### Externalizing Configuration
## 6. Logs
## 7. Disposability
## 8. Backing Services
## 9. Environment Parity
### Time
### People
### Resource
### Every Commit Is a Candidate for Deployment
## 10. Adminitrative Processes
## 11. Port Binding
### Avoiding Container-Determined Ports
### Avoiding Micromanaging Port Assignments
### Applications are Backing Services
## 12. Stateless Processes
### A Practical Definition of Stateless
### The Share-Nothing Pattern
### Data Caching
## 13. Concurrency
## 14. Telemetry
## 15. Authentication and Authorization
## 16. A Word on Cloud Native
### What Is Cloud Native?
### Why Cloud Native?
### The Purist vs the Pragmatist
## 17. Summary

