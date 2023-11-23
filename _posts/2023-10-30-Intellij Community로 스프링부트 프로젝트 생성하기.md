---
layout: post
title: Spring Initializr로 프로젝트 생성하기
date: 2023-10-30 
categories: [Spring]
tags: [Spring, Spring Boot, 환경설정]
---
IntelliJ Community를 사용하는데 스프링 프로젝트 생성을 지원하지 않는 거 같아서 작성하는 글  
Spring Initializr 사이트를 가면 쉽게 스프링 프로젝트 생성이 가능하다.

# Spring Initializr 사용하기
- [**Spring Initializr 바로가기**](https://start.spring.io/)

<figure>
    <img src="/48089347-eafa-43b6-a649-6ba372f14a7a.png" alt="spring initializr site image" />
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
  <img src="/3c9dab2e-a16d-4836-bb7b-e202b77c6c5f.png" alt="Dependencies" />
  <figcaption>Dependencies</figcaption>
</figure>

- **GENERATE**: 생성 버튼 프로젝트를 ZIP 파일로 다운로드 받을 수 있다.
- **EXPLORE**: 코드를 볼 수 있다.
<figure>
  <img src="/1c20bdf6-71ab-49e8-9087-6ee46ec3fcf6.png" alt="EXPLORE" />
  <figcaption>EXPLORE</figcaption>
</figure>

- **SHARE**: 공유 버튼 링크를 생성
<figure>
  <img src="/6a3eb6ee-990c-429a-96c9-50025e0cf17a.png" alt="SHARE" />
  <figcaption>SHARE</figcaption>
</figure>

**Refrerence**
- [spring.io](https://spring.io/guides/gs/spring-boot/)
- [start.spring.io](https://start.spring.io/)