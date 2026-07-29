# 🚀 Codyssey Docker & Git Practice Mission

> 본 문서는 리눅스 터미널, Docker 컨테이너, Git/GitHub를 활용하여 개발 워크스테이션을 구축하고 정적 웹 서버를 컨테이너화한 실습 기록입니다.

---

## 1) 실행 환경
- **OS**: macOS 15.7.4
- **Shell**: zsh
- **Docker**: 28.5.2
- **Git**: 2.53.0

---

## 2) 수행 체크리스트
- [x] 터미널 기본 조작 및 폴더 구성
- [x] 파일 및 디렉토리 권한 변경 실습
- [x] Docker 설치 및 데몬 점검
- [x] hello-world 및 ubuntu 컨테이너 실행 실습
- [x] Dockerfile 커스텀 작성 및 이미지 빌드
- [x] 포트 매핑을 통한 웹 서버 실행 및 접속 검증
- [x] 바인드 마운트 반영 확인
- [x] Docker 볼륨 생성 및 데이터 영속성 검증
- [x] Git 사용자 설정 및 GitHub 연동

---

## 3) 프로젝트 개요 및 실행 방법

### 📌 개요
이 프로젝트는 HTML 웹페이지를 Docker와 Nginx를 이용해 컨테이너화하고, 포트 매핑과 볼륨 영속성, 그리고 Git을 통한 버전 관리까지 수행한 실습입니다.

### 🚀 실행 방법 (Build & Run)
터미널에서 프로젝트 루트 디렉토리로 이동한 후 아래 명령어를 입력합니다.

```bash
# 1. 커스텀 이미지 빌드
docker build -t docker-web-practice:latest .

# 2. 포트 매핑으로 컨테이너 실행
docker run -d --name my-web -p 8080:80 docker-web-practice:latest

# 3. 실행 중인 컨테이너 확인
docker ps

# 4. 접속 테스트
curl http://localhost:8080
