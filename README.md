# report-match

- 리포트 매칭 프로젝트

## 시작하기

```bash
git clone https://github.com/kidcat2/report-match.git
cd report-match
```

## 개발 환경

- 추후 업데이트 예정

## 라이선스

- 추후 업데이트 예정


### 파일 분류

샘플
- 테스트 데이터 산출
    - 산출 내역서, 증빙 자료 원본 => 기업이 제출한 것
    - 정산 내역서 : 정답지 샘플
- 업무 기준 정의서 
    - 내가 정산 내역서를 정리하는 기준
- 정답지
    - 기업이 보내준 산출 내역서, 증빙 자료 원본, 샘플 채운 내용, etc => 맞게 정리한 것


** 파이프라인

1. 사용자가 웹 브라우저에 기업 파일을 넣는다 company.zip
2. 기업 파일을 전처리 한다. (PNG) --> company_file(img format + docs, hwp format)
3. 기업 파일(전처리) + Prompt + json 양식 --> company.json
4. 클로드 API에게 (company.json + 카테고리 체계.md + prompt) --> company_category.md 완성
5. 클로드 API에게 (company_category.md + sample.xlsx + 엑셀 매핑규칙.md + prompt) --> company_final.xlsx 완성


** 기준 파일



1. 카테고리 체계.md (task01_output) :
    - 클로드 API는 총 (카테고리 체게.md + )