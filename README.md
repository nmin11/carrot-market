# Carrot Market

노마드코더의 당근마켓 클론코딩을 학습한 레포지토리입니다.

<br>

## Server 구동 방법

- `pscale connect carrot-market`
  - db url이 바뀔 경우, **schema.prisma**에 적용
- `npx prisma studio`

<br>

## 추가로 알아둬야 할 명령어

- `npx prisma db push` : schema를 planet scale과 연동하기 위한 작업
- `npx prisma generate` : db에 접속하는 client 생성

<br>

## SWR

- 요청 시에는 캐시로부터 데이터를 로드하며, API를 통해 꾸준히 최신화된 데이터를 받아옴
- useSWR 의 mutate 함수를 활용하면 Optimistic UI Update 구현 가능
  - unbound mutate 함수를 활용하면 다른 화면의 데이터도 변경 가눙
- Redux와 같은 상태 관리 라이브러리
