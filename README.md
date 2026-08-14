# DawooCivilLISP

AutoCAD와 ZWCAD 2024에서 사용하는 토목 설계용 AutoLISP 도구 모음입니다.

## 지원 환경

- AutoCAD 2021 이상 (Windows)
- ZWCAD 2024 (Windows)

## 설치

1. [최신 릴리스](https://github.com/leecycle/DawooCivilLISP/releases/latest)에서 `DawooCivilLISP.1.0.4.zip`을 내려받습니다.
2. ZIP 압축을 완전히 풉니다.
3. `DawooCivilLISP_Install.cmd`를 실행합니다.
4. AutoCAD 또는 ZWCAD를 다시 시작합니다.

기본 설치 폴더는 `C:\DAWOO\CivilLISP`입니다. 기존 신뢰할 수 있는 위치와 APPLOAD 시작세트 항목은 유지하면서 DawooCivilLISP 경로만 중복 없이 등록합니다.

## 1.0.4 업데이트 개선

- 기존 설치 폴더 전체를 백업한 뒤 새 패키지로 완전히 교체
- 이전 아이콘과 하위 폴더 파일이 남지 않도록 정리
- 파일 교체 실패 시 기존 설치 자동 복원
- 설치·업데이트·복원 팝업을 한글로 통일
- ANSI(CP949) 한글 인코딩 유지

## 주요 명령

- `VV` - 거리 측정 및 누계
- `GST` - 선형 STA/NO 측점 조회
- `RC` - 선, 폴리선, 호, 스플라인 방향 반전
- `DWCHELP` - 도움말 열기
- `DWCVER` - 설치 버전 확인
- `DWCUPDATE` - 최신 버전 확인 및 업데이트
- `DWCROLLBACK` - 전체 백업에서 이전 버전 복원

> 토목좌표 기본 단위: 도면거리 1 = 1 m
