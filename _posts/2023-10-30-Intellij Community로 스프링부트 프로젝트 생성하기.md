---
layout: post
title: "Spring Initializr로 프로젝트 생성하기"
date: 2023-10-30 
categories: [Spring]
tags: [Spring, Spring Boot, 환경설정]
---

<style>
.img-link {
  display: block;
}
</style>

IntelliJ Community를 사용하는데 스프링 프로젝트 생성을 지원하지 않는 거 같아서 작성하는 글  
Spring Initializr 사이트를 가면 쉽게 스프링 프로젝트 생성이 가능하다.


# Spring Initializr 사용하기
- [Spring Initializr 바로가기](https://start.spring.io/)

<figure>
    <img src="/assets/img/2023-10-30/spring-initializr.png" alt="spring initializr site image" />
</figure>

- **Project**: 빌드 도구를 선택한다.
- **Language**: 프로그래밍 언어를 선택한다.
- **Spring Boot**: 스프링 부트의 버전을 선택한다.
- **Project Metadata**
  - **Group**: 팀 이름, 회사 이름
  - **Atifact**: 프로젝트 이름
  - **Name**: 어플리케이션 이름
  - **Description**: 어플리케이션 설명
  - **Package name**: 그룹.아티팩트 ex) com.example.demo로 작성된다.
  - **Packaging**: 배포 방식
- **Dependencies**: 외부 라이브러리 관리, 쉽게 추가할 수 있다.
<figure>
  <img src="/assets/img/2023-10-31/dependencies.png" alt="Dependencies" />
  <fication>Dependencies</fication>
</figure>

- **GENERATE**: 생성 버튼 프로젝트를 ZIP 파일로 다운로드 받을 수 있다.
- **EXPLORE**: 코드를 볼 수 있다.
<figure>
  <img src="/assets/img/2023-10-31/explore.png" alt="EXPLORE" />
  <fication>EXPLORE</fication>
</figure>

- **SHARE**: 공유 버튼 링크를 생성
<figure>
  <img src="/assets/img/2023-10-31/share.png" alt="SHARE" />
  <fication>SHARE</fication>
</figure>