# DawooCivilLISP

## 설명

DawooCivilLISP는 토목·CAD 실무에서 반복되는 도면 작성, 편집 및 조회 작업을 빠르고 일관되게 처리하는 AutoLISP 도구 모음입니다. AutoCAD와 ZWCAD 2024를 하나의 배포 파일로 지원하며 설치, 자동 로드, 메뉴, 업데이트 및 복원 기능을 제공합니다.

## 지원 환경

- AutoCAD 2015~2024 (Windows)
- ZWCAD 2024 (Windows)
- 설치 폴더: `C:\DAWOO\CivilLISP`
- LISP 원본 인코딩: ANSI(CP949)

## 주요 기능

- 레이어, 치수, 문자 및 표고 편집
- 중심선·수직선 작성과 선형 방향 변경
- 면적, 좌표, 거리 및 누계 조회
- Excel 좌표 가져오기·내보내기
- AutoCAD용 VLX와 ZWCAD용 ZELX 자동 판별
- 정식·시험 업데이트 채널, 전체 백업, 실패 시 자동 복원
- 전체 기능 메뉴, 도구막대 및 PDF 도움말
- 모든 DawooCivilLISP 명령 실행 시 첫 줄에 명령어와 기본 기능 설명 표시
- 토목 작업 명령은 `DWXY`, `DWFW`, `DWVV`처럼 `DW` 접두어로 통일

> 토목좌표 기본 단위는 도면거리 `1 = 1.00 m`입니다.

## 설치 방법

1. [최신 릴리스](https://github.com/leecycle/DawooCivilLISP/releases/latest)에서 `DawooCivilLISP.*.zip`을 내려받습니다.
2. ZIP을 완전히 압축 해제합니다.
3. 압축을 푼 폴더에서 `Install.exe`를 실행합니다.
4. 설치 완료 후 AutoCAD 또는 ZWCAD를 다시 시작합니다.
5. `DWCOP`에서 버전 정보와 업데이트 채널을 확인합니다.
6. `DWCHELP`를 실행하면 PDF 도움말이 열립니다.

최초 설치 때만 기존 설정을 보존하면서 신뢰 경로, APPLOAD 시작세트, 메뉴와 도구막대를 등록합니다.

## AutoCAD와 ZWCAD를 함께 사용하는 경우

- 두 CAD는 같은 `C:\\DAWOO\\CivilLISP` 폴더를 사용합니다.
- AutoCAD는 `DawooCivilLISP_*.vlx`, ZWCAD 2024는 `DawooCivilLISP_*.zelx`를 불러옵니다.
- 메뉴 등록 상태는 제품별로 확인하며 없는 경우에만 복구합니다.
- 한 번 설치하거나 업데이트하면 두 제품용 파일이 함께 교체됩니다.

## 업데이트

1. `DWCOP`에서 정식 또는 시험 채널을 선택합니다. 기본값은 정식 채널입니다.
2. `DWCUPDATE`를 실행합니다.
3. 정식 채널은 일반 Release, 시험 채널은 Pre-release를 포함해 최신 버전을 확인합니다.
4. 업데이트 승인 후 도면을 저장하고 AutoCAD와 ZWCAD를 종료합니다.
5. 기존 설치 전체를 백업하고 새 패키지를 검증한 뒤 교체합니다.
6. 실패하면 기존 설치 전체를 자동 복원합니다.

업데이트는 최초 설치 때 등록한 신뢰 위치와 시작세트를 다시 변경하지 않으며, DawooCivilLISP 메뉴 존재 여부만 확인합니다.

## 메뉴와 도움말

- `DWCOP`: 설치·백업 폴더 열기, 버전·채널 확인, 다시 불러오기, 채널 설정
- `DWCUPDATE`: 현재 채널의 최신 버전 확인 및 업데이트
- `DWCROLLBACK`: 백업된 이전 버전으로 복원
- `DWCTOOLBAR`: 도구막대 표시
- `DWCTOOLBARRESET`: 메뉴와 도구막대 다시 등록
- `DWCHELP`: PDF 도움말 열기

전체 명령과 사용 방법은 설치 폴더의 `DawooCivilLISP_Help.pdf`를 참고하십시오.

## 버전별 변경사항

- 1.3.1: CR 문자 사각 중심 이동 명령 추가
- 1.3.2: GUI 신규 설치와 전체 백업 적용
- 1.3.3: AutoCAD PNG 아이콘 절대경로 연결
- 1.3.4: 모든 사용자 명령의 첫 줄 기능 설명 추가
- 1.3.5: TER·CR·VV 오류 수정
- 1.3.6: 설치형 Updater EXE, CAD 종료 확인과 실패 자동 복원 적용
- 1.4.0: 1.3.1~1.3.6 개선사항을 정식 적용하고 배포본에서 기능 원본 LSP 제외
- 1.5.11: 토목 작업 명령을 DW 접두어 체계로 통일하고 ELRESET 명령 삭제
- 1.6.0: 속성 도곽 Excel 통합, SheetSet 필드와 지번 정리 개선사항을 정식 적용

## 주의 사항

- 설치 또는 업데이트 중에는 AutoCAD와 ZWCAD를 모두 종료해야 합니다.
- ZIP 내부에서 바로 실행하지 말고 반드시 완전히 압축 해제하십시오.
- LISP 원본을 수정할 때는 ANSI(CP949) 인코딩을 유지하십시오.
- 배포 ZIP에는 AutoCAD용 VLX와 ZWCAD용 ZELX가 모두 포함되어야 합니다.
- 문제가 생기면 CAD를 종료한 뒤 `DWCROLLBACK`을 사용하거나 배포본으로 다시 설치하십시오.
