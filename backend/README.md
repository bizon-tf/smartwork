# smartwork backend

## 스프링 부트 프로파일 설정

  1. 기본 프로파일: local로 설정 (application.yml)
  2. 생성된 프로파일 파일들:
    - `application-local.yml`: H2 메모리 DB, DevTools 활성화, 상세 로깅
    - `application-dev.yml`: PostgreSQL, 개발 서버용 설정
    - `application-stage.yml`: 스테이징 환경 설정, 성능 최적화
    - `application-prod.yml`: 프로덕션 환경 설정, 최소 로깅, 보안 강화

  프로파일 실행 방법:
  # 기본 (local) 프로파일로 실행
  ```bash
  ./gradlew bootRun
  ```

  # 특정 프로파일로 실행
  ```bash
  ./gradlew bootRun
  --args='--spring.profiles.active=dev'
  ./gradlew bootRun
  --args='--spring.profiles.active=stage'
  ./gradlew bootRun
  --args='--spring.profiles.active=prod'
  ```


## test report
- JaCoCo 플러그인 추가 (버전 0.8.13 - Java 24 지원)
- 리포트 위치: `build/reports/jacoco/test/`
```bash
./gradlew test jacocoTestReport
```