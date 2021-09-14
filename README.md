## About Project
- REST API 를 통한 데이터 연동 및 활용.
- 연도별 영화내역을 리스트업하고, 원하는 영화를 클릭했을때 내 주변에서 가장 가까운 영화관을 소개하는 사이트
- 데이터출처 [영화진흥위원회](http://www.kobis.or.kr/kobisopenapi/homepg/apiservice/searchServiceInfo.do?serviceId=searchMovieInfo).

## Todo
- [X] 프론트 화면기획 및 구축
- [X] 프론트 Tailwind CSS프레임워크 Setup
- [X] 프론트 디자인 작업 (기본 메인 페이지 작업만 수행하자)
- [ ] 프론트 ReactJS 프레임워크 (express / next) 도입 검토
- [ ] 프론트 ReactJS SPA + Route
- [ ] 프론트 ReactJS 리덕스 : 단일스토어 / 읽기전용 / 순수함수 준수
- [ ] 프론트 ReactJS 코드스플리팅
- [ ] 백앤드 php - Laravel RestAPI 기초 작업 이후, 백앤드 교체
- [ ] 백앤드 springboot 
- [ ] 기능 - 지도 API선정 :: 네이버 API활용
- [ ] 기능 - 지도 마커 표기
- [ ] 기능 - 전체 측정소정보 목록(getMsrstnList) 데이터 응답받아 받아 dmXY 값을 기준으로 전체측정소 데이터 스케쥴러 작성 및 마커 표기

## Setup His
### 1) Tailwind 
```
1.Tailwindscss 설치
> npm install -D tailwindcss@npm:@tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9

2. CRACO 설치
> npm install @craco/craco

3.pakage.json start / build / test 수정
{
    // ...
    "scripts": {
-     "start": "react-scripts start",
-     "build": "react-scripts build",
-     "test": "react-scripts test",
+     "start": "craco start",
+     "build": "craco build",
+     "test": "craco test",
      "eject": "react-scripts eject"
    },
  }

3.craco.config.js 설정
module.exports = {
  style: {
    postcss: {
      plugins: [
        require('tailwindcss'),
        require('autoprefixer'),
      ],
    },
  },
}

4.tailwind.config.js 생성
> npx tailwindcss-cli@latest init

5.tailwind.config.js 설정
  module.exports = {
-   purge: [],
+   purge: ['./src/**/*.{js,jsx,ts,tsx}', './public/index.html'],
    darkMode: false, // or 'media' or 'class'
    theme: {
      extend: {},
    },
    variants: {
      extend: {},
    },
    plugins: [],
  }

6. ./src/index.css 수정
@tailwind base;
@tailwind components;
@tailwind utilities;


```

## Based on following plugins or services
- RestAPI
- ReactJS
- Npm 7.21.0 / Yarn 1.22.10
- Tailwind css v2.2.14[Tailwindcss](https://tailwindcss.com/).
- Laravel v7.3
- Laravel - MongoDB [laravel-mongodb#query-builder](https://github.com/jenssegers/laravel-mongodb#query-builder).
- Laravel - Schedul
- Laravel - Job 