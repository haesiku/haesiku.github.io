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

### Original 12 Factors에 최신 지침을 추가한 Beyond 12 Factors도 알아보자.
1. One Codebase, One Application
2. API First
3. Dependency Management
4. Design, Build, Release, And Run
5. Configuration, Credentials, and Code
6. Logs
7. Disposability
8. Backing Services
9. Environment Parity
10. Administrative Processes
11. Port Binding
12. Stateless Processes
13. Concurrency
14. Telemetry
15. Authentication and Authorization


# Contents
## 1. One Codebase, One Application
## 2. API First
### Why API First?
### Building Services API First
## 3. Dependency Management
### Reliance on the Mommy Server
### Modern Dependency Management
## 4. Design, Build, Release, Run
### Design
### Build
### Release
### Run
## 5. Configuration, Credentials, and Code
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

