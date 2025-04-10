# Study Deploy Infra

Cafe24 서버용 배포 자동화 구성입니다.  
GitHub Actions와 Shell Script 기반으로 구성됩니다.

## 구성 요소

- infra/
  - scripts/
    - deploy-backend.sh
    - deploy-frontend.sh
  - nginx/
    - default.conf
  - github-actions/
    - deploy-backend.yml
    - deploy-frontend.yml


## 배포 방식

1. GitHub Actions 트리거
2. SSH를 통해 Cafe24 서버 접속
3. 백엔드/프론트 각각 빌드 결과 전송
4. Nginx 설정 반영 및 서비스 재시작

## 서버 기본 구조 (예시)

| 경로                | 용도               |
|---------------------|--------------------|
| `/home/ubuntu/backend/` | 백엔드 .jar 위치     |
| `/var/www/html/`        | 프론트 정적 파일 위치 |
| `/etc/nginx/`           | Nginx 설정 경로      |

## 관련 레포

- study-deploy-backend
- study-deploy-frontend
