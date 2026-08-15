# DawooCivilLISP

## 설명

DawooCivilLISP는 토목·CAD 실무에서 반복되는 도면 작성, 편집 및 조회 작업을 빠르고 일관되게 처리하기 위한 통합 AutoLISP 도구 모음입니다. 하나의 배포 파일로 AutoCAD와 ZWCAD 2024를 함께 지원하며 설치, 자동 로드, 메뉴 등록, 업데이트 및 복원 기능을 제공합니다.

## 지원 환경

- AutoCAD 2021 이상 (Windows)
- ZWCAD 2024 (Windows)
- 공용 설치 폴더: `C:\DAWOO\CivilLISP`
- LISP 원본 인코딩: ANSI(CP949)

## 주요 기능

- 선택 객체 및 선택 레이어 켜기·끄기
- 문자, 치수 및 표고 편집
- 선형 작성과 객체 방향 반전
- 면적, 좌표, 거리 및 누계 조회
- 선형의 STA·NO 측점 조회
- Excel 좌표 내보내기·가져오기
- AutoCAD와 ZWCAD 자동 판별 및 전용 컴파일 파일 로드
- 프로그램 내 자동 업데이트와 이전 버전 복원
- 전체 기능 메뉴, 도구막대 및 PDF 도움말 제공

> 토목좌표 기본 단위는 도면거리 `1 = 1.00 m`입니다.

## 설치 방법

1. [최신 릴리스](https://github.com/leecycle/DawooCivilLISP/releases/latest)에서 `DawooCivilLISP.*.zip`을 내려받습니다.
2. ZIP을 완전히 압축 해제합니다.
3. 압축을 푼 폴더에서 `DawooCivilLISP_Install.cmd`를 실행합니다.
4. 설치가 끝나면 AutoCAD 또는 ZWCAD를 다시 시작합니다.
5. 명령창에서 `DWCVER`를 실행해 현재 CAD와 DawooCivilLISP 버전을 확인합니다.
6. `DWCHELP`를 실행하면 PDF 도움말이 열립니다.

최초 설치 프로그램은 기존 설정을 지우지 않고 다음 항목을 중복 없이 추가합니다.

- `C:\DAWOO\CivilLISP` 신뢰 경로
- `C:\DAWOO\CivilLISP\DawooCivilLISP.lsp` 시작하기 세트
- 현재 CAD에 DawooCivilLISP 메뉴가 없을 때 메뉴와 도구막대 자동 등록

## AutoCAD와 ZWCAD를 함께 사용하는 경우

두 CAD는 같은 `C:\DAWOO\CivilLISP` 설치 폴더를 사용합니다.

- AutoCAD에서는 `DawooCivilLISP_*.vlx`를 자동으로 불러옵니다.
- ZWCAD 2024에서는 `DawooCivilLISP_*.zelx`를 자동으로 불러옵니다.
- 메뉴 등록 상태는 AutoCAD와 ZWCAD에서 각각 확인하며, 없는 경우에만 자동 등록합니다.
- 한 번 설치하거나 업데이트하면 AutoCAD용과 ZWCAD용 파일이 함께 교체됩니다.

## 업데이트

1. CAD 명령창에서 `DWCUPDATE`를 실행합니다.
2. 현재 버전과 GitHub의 최신 정식 릴리스를 비교합니다.
3. 업데이트를 승인한 뒤 작업 중인 도면을 저장합니다.
4. AutoCAD와 ZWCAD를 모두 완전히 종료합니다.
5. 기존 설치 폴더 전체를 백업하고 새 패키지를 검증한 뒤 교체합니다.
6. 설치에 실패하면 전체 백업을 자동으로 복원합니다.

업데이트는 최초 설치 때 등록된 신뢰 위치와 시작하기 세트를 다시 변경하지 않습니다. 기존 CAD 설정과 다른 메뉴도 유지하며 DawooCivilLISP 메뉴가 있는지만 확인합니다.

## 메뉴와 도움말

- `DWCTOOLBAR`: DawooCivilLISP 도구막대 표시
- `DWCTOOLBARRESET`: 메뉴와 도구막대 다시 등록
- `DWCHELP`: PDF 도움말 열기
- `DWCUPDATE`: 최신 정식 버전 확인 및 업데이트
- `DWCROLLBACK`: 백업된 이전 버전으로 복원
- `DWCVER`: 현재 CAD와 설치 버전 확인
- `DWCRELOAD`: DawooCivilLISP 다시 불러오기

전체 명령과 사용 방법은 설치 폴더의 `DawooCivilLISP_Help.pdf`에서 확인할 수 있습니다.

## 주의 사항

- 설치 또는 업데이트 중에는 AutoCAD와 ZWCAD를 모두 종료해야 합니다.
- ZIP 내부에서 설치 파일을 바로 실행하지 말고 반드시 완전히 압축 해제하십시오.
- LISP 원본을 수정할 때는 ANSI(CP949) 인코딩을 유지하십시오.
- 배포 ZIP에는 AutoCAD용 VLX와 ZWCAD용 ZELX가 모두 포함되어야 합니다.
- 문제가 생기면 CAD를 종료한 뒤 마스터 설치본으로 다시 설치하거나 `DWCROLLBACK`을 사용하십시오.
