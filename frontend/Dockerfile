# 프론트엔드용 Dockerfile - 빌드된 결과물 사용
FROM nginx:1.25-alpine

# Nginx 설정 파일 복사 (선택사항)
# COPY nginx.conf /etc/nginx/nginx.conf

# CI에서 빌드된 dist 폴더를 Nginx 서빙 디렉토리로 복사
COPY dist/ /usr/share/nginx/html/

# 포트 노출
EXPOSE 80

# Nginx 실행
CMD ["nginx", "-g", "daemon off;"]