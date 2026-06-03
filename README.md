[README.md](https://github.com/user-attachments/files/28536002/README.md)
# MANUAL 영어학원 PRO · AI Edition

영어 학원 전용 성적 관리 + AI 분석 웹 애플리케이션입니다.

## 주요 기능

- **성적 입력 & AI 분석** — 학생별 시험 답안 입력, Anthropic Claude API를 활용한 문항별 오답 원인 및 해결책 자동 생성
- **대시보드** — 전체 학생 평균, 90점 이상 비율, 시험 기록 현황 한눈에 확인
- **학생 관리** — 반/학년별 학생 등록 및 관리
- **문항 분석** — 문항별 오답률 히트맵 및 통계
- **성적 랭킹** — 반별 순위표
- **회차 비교** — 시험 회차 간 성적 추이 분석
- **리포트 출력** — 학생별 PDF 성적표 생성 (html2pdf)

## 사용 방법

1. 사이드바 하단 **🔑 ANTHROPIC API KEY** 입력란에 본인의 API 키를 입력합니다.
   - API 키는 브라우저 로컬에만 저장되며 외부로 전송되지 않습니다.
   - API 키 발급: [console.anthropic.com](https://console.anthropic.com)
2. **학생 관리** 또는 **➕ 학생 추가** 버튼으로 학생을 등록합니다.
3. **성적 입력 + AI** 탭에서 시험 정보와 답안을 입력합니다.
4. **🤖 AI 코멘트 생성** 버튼으로 오답 분석 코멘트를 자동 생성합니다.
5. **리포트 출력** 버튼으로 PDF 성적표를 다운로드합니다.

## 기술 스택

- Vanilla HTML / CSS / JavaScript (단일 파일, 프레임워크 없음)
- [Chart.js](https://www.chartjs.org/) — 성적 추이 차트
- [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) — PDF 출력
- [Anthropic Claude API](https://www.anthropic.com/) — AI 오답 분석

## 데이터 저장

모든 학생 데이터는 브라우저의 **LocalStorage**에 저장됩니다. 서버나 외부 DB를 사용하지 않습니다.

- 사이드바 하단 **💾 DB 백업** 버튼으로 JSON 파일로 내보낼 수 있습니다.
- **📂 DB 불러오기** 버튼으로 백업 파일을 복원할 수 있습니다.

## 배포

GitHub Pages를 통해 정적 호스팅으로 바로 배포 가능합니다.

```
저장소 Settings → Pages → Branch: main / (root) → Save
```

배포 후 접속 URL 형식: `https://[유저명].github.io/[저장소명]/`

## 라이선스

본 프로젝트는 개인/학원 내부 사용 목적으로 제작되었습니다.
