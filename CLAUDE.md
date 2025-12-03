# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

Docker 기반 PocketBase 백엔드 서비스. PocketBase는 실시간 DB, 인증, 파일 저장소를 제공하는 오픈소스 백엔드.

## 주요 명령어

```bash
# 컨테이너 시작
docker compose up -d

# 컨테이너 중지
docker compose down

# 로그 확인
docker compose logs -f pocketbase

# 컨테이너 재빌드 (버전 업데이트 시)
docker compose up -d --build
```

## 아키텍처

- **pb_data/**: SQLite DB 저장소 (gitignore 대상)
- **pb_migrations/**: DB 마이그레이션 파일
- **pb_hooks/**: JavaScript 훅 (API 확장)
- **pb_public/**: 정적 파일

## 접속 정보

- 호스트 포트: `8090`
- Public: `http://localhost:8090`
- Admin UI: `http://localhost:8090/_/`
- API: `http://localhost:8090/api/`

## PocketBase 버전

Dockerfile ARG `PB_VERSION`으로 관리 (현재: 0.34.1)
