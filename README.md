# 실시간 강의 노트

수업을 실시간으로 받아쓰고, AI(Claude)가 정리 노트를 써주는 웹 앱.

- 주소: https://notes.dailyradar.app
- 받아쓰기: 브라우저 음성인식 (Chrome · Edge, 한국어/영어/프랑스어/중국어)
- AI 정리: 각자의 Claude API 키 사용 (⚙ 설정). 키는 그 사람 브라우저에만 저장되고 Anthropic API로만 전송됨
- 강의자료 첨부: PDF · PPTX · DOCX · TXT — 지금 말하는 내용과 관련된 페이지만 골라 정리에 참고
- 서버 없음: `index.html` 하나로 동작하는 정적 사이트 (GitHub Pages)

## 구성
- `index.html` — 앱 전체 (Claude 안에서 열면 Claude 받아쓰기·정리, 사이트에서 열면 Chrome 받아쓰기 + 본인 API 키)
- `about.html` — 이용 안내 · 개인정보
- `vendor/` — 외부 라이브러리 고정 버전 사본 (marked 12.0.2, DOMPurify 3.1.6, pdf.js 3.11.174, JSZip 3.10.1, html2canvas 1.4.1, jsPDF 2.5.1). 각 라이브러리의 라이선스를 따름
- `manifest.webmanifest`, 아이콘 — 홈 화면에 추가하면 앱처럼 열림
- `og.png` — 카카오톡·SNS 링크 미리보기
