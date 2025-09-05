# 멀티스테이지 빌드를 사용한 프론트엔드 Dockerfile
FROM node:24.7.0-alpine AS builder

# 작업 디렉토리 설정
WORKDIR /app

# package.json과 yarn.lock 복사
COPY package.json yarn.lock ./

# 의존성 설치
RUN yarn install --frozen-lockfile

# 소스코드 복사
COPY . .

# 프로덕션 빌드
RUN yarn build

# Nginx를 사용한 프로덕션 이미지
FROM nginx:1.25-alpine

# Nginx 설정 파일 복사 (선택사항)
# COPY nginx.conf /etc/nginx/nginx.conf

# 빌드된 파일들을 Nginx 서빙 디렉토리로 복사
COPY --from=builder /app/dist /usr/share/nginx/html

# 포트 노출
EXPOSE 80

# Nginx 실행
CMD ["nginx", "-g", "daemon off;"]