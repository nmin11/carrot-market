# Carrot Market

노마드코더의 당근마켓 클론코딩을 학습한 레포지토리입니다.

<br>

## Server 구동 방법

- `pscale connect carrot-market`
  - db url이 바뀔 경우, **schema.prisma**에 적용
- `npx prisma studio`

<br>

## 추가로 알아둬야 할 명령어

- `prisma db push` : schema를 planet scale과 연동하기 위한 작업
- `npx prisma generate` : db에 접속하는 client 생성
