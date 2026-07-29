##1)실행 환경
##2) 수행 체크리스트


# Docker 기반 정적 웹 서버 컨테이너화

이 프로젝트는 HTML 웹페이지를 Docker와 Nginx로 실행한 실습입니다.

## 실행 방법

docker build -t my-web:1.0 .
docker run -d -p 8080:80 --name my-web-container my-web:1.0

접속 주소:
http://localhost:8080

##3)수행 로그 파일

- logs/docker-ps.log
- logs/docker-images.log
- logs/curl-result.log
- logs/terminal-ops.log

## GitHub

https://github.com/allinoneai2-jyunhui/ia-codyssey.git
