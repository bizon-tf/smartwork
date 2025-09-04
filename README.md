# smartwork : 사내시스템리뉴얼프로젝트 (T/F)

[![메인 브랜치 CI](https://github.com/bizon-tf/smartwork/actions/workflows/main-ci.yml/badge.svg)](https://github.com/bizon-tf/smartwork/actions/workflows/main-ci.yml)
[![PR 체크](https://github.com/bizon-tf/smartwork/actions/workflows/pr-check.yml/badge.svg)](https://github.com/bizon-tf/smartwork/actions/workflows/pr-check.yml)
[![보안 스캔](https://github.com/bizon-tf/smartwork/actions/workflows/security.yml/badge.svg)](https://github.com/bizon-tf/smartwork/actions/workflows/security.yml)
[![릴리스](https://github.com/bizon-tf/smartwork/actions/workflows/release.yml/badge.svg)](https://github.com/bizon-tf/smartwork/actions/workflows/release.yml)

## 프로젝트 소개
사내시스템 스마트워크, 통합 어드민을 스마트워크 플랫폼으로 통합하는 리뉴얼 프로젝트(아마도..)

## 기술 스택

### Frontend
![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7.1-646CFF?style=flat-square&logo=vite&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-3.2-729B1B?style=flat-square&logo=vitest&logoColor=white)

### Backend
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5.5-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-2.2-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-24-007396?style=flat-square&logo=openjdk&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-9.0-02303A?style=flat-square&logo=gradle&logoColor=white)

### Database
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-17.x-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![H2](https://img.shields.io/badge/H2_Database-Dev/Test-0000BB?style=flat-square)

## 빠른 시작

### (Optional) 가상홤경 설정
```bash
cd frontend
nodeenv --node=24.7.0 env-24.7.0 # 가상환경 설정
source ./env-24.7.0/bin/activate # 가상환경 활성화
# 가상환경 내에서 yarn 설치
npm install -g yarn
```

### Frontend 개발
```bash
cd frontend
yarn install
yarn dev
```

### Backend 개발
```bash
cd backend
./gradlew bootRun
```

### 테스트 실행
```bash
# Frontend
cd frontend && yarn test

# Backend
cd backend && ./gradlew test
```
