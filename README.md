# GilliLab PocketBase

Docker 기반 PocketBase 백엔드 서비스

## 시작하기

```bash
# 컨테이너 시작
docker compose up -d

# 컨테이너 중지
docker compose down
```

## 접속

- **Public**: http://localhost:8090
- **API**: http://localhost:8090/api/
- **Admin UI**: http://localhost:8090/\_/

## 디렉토리 구조

| 디렉토리         | 설명                     |
| ---------------- | ------------------------ |
| `pb_data/`       | SQLite DB 저장소         |
| `pb_migrations/` | DB 마이그레이션 파일     |
| `pb_hooks/`      | JavaScript 훅 (API 확장) |
| `pb_public/`     | 정적 파일                |

## PocketBase 버전 업데이트

1. `Dockerfile`에서 `PB_VERSION` 수정
2. 재빌드: `docker compose up -d --build`

## 로그

```bash
docker compose logs -f pocketbase
```
