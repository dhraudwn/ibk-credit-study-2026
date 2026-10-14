# 여신 스터디

2026 하반기 IBK 책임자시험 여신 학습 웹페이지입니다.

- 16개 파트의 원본 연습문제 314개와 변형문제 314개
- 답안 선택 즉시 채점, 공식 해설, 본문 요약과 선지별 근거
- 본문과 문제 원문 이미지, 정오표 반영
- 파트를 골고루 포함하는 40문항 모의고사
- 진도·오답·북마크·시험 기록을 브라우저에 저장
- 학습 기록 JSON 백업 및 복원

학습 기록은 사용한 기기와 브라우저에 저장됩니다. 다른 기기로 옮길 때는 설정에서 백업 및 복원을 사용하세요.

## 배포 및 소스

이미지와 소스 전체를 `study-site.tar.gz.part00`부터 `part06`까지 7개 파일로 나누어 보관합니다. GitHub Actions가 순서대로 합치고 압축을 풀어 7개 검사를 실행한 뒤 `dist`를 GitHub Pages에 배포합니다.

로컬에서 소스 확인:

```bash
cat study-site.tar.gz.part* > study-site.tar.gz
tar -xzf study-site.tar.gz
node --test work/core.test.mjs
```

`dist`는 외부 API 없이 동작하는 HTML·CSS·JavaScript 정적 앱입니다.
