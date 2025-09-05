# 백엔드용 Dockerfile - Spring Boot 애플리케이션
FROM eclipse-temurin:24-jre-alpine

# 작업 디렉토리 설정
WORKDIR /app

# curl 설치 (헬스체크용)
RUN apk add --no-cache curl

# 비루트 사용자 생성
RUN addgroup -S spring && adduser -S spring -G spring

# JAR 파일 복사 (CI에서 빌드된 파일을 사용)
COPY build/libs/*[!-plain].jar app.jar

# 파일 소유권 변경
RUN chown spring:spring app.jar

# 비루트 사용자로 실행
USER spring

# JVM 메모리 설정 및 기타 최적화 옵션
ENV JAVA_OPTS="-Xmx512m -Xms256m -XX:+UseContainerSupport -XX:MaxRAMPercentage=75.0"

# 포트 노출
EXPOSE 8080

# 헬스체크 추가
HEALTHCHECK --interval=30s --timeout=3s --start-period=30s --retries=3 \
  CMD curl -f http://localhost:8080/actuator/health || exit 1

# 애플리케이션 실행
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar app.jar"]