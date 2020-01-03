---
title: (blog) google-analytics 추가
date: "2020-01-03T12:29:03.284Z"
description: "google-analytics 추가"
---

블로그에 유입되는 정보를 알고 싶어서 google analytics를 추가합니다.
google analytics는 추적 ID 당 한달에 1000만건의 조회수를 무료로 제공합니다.

### google analyitics 가입

google analytics에 가입을 하고 추적 ID를 발급받습니다.(UA-XXXXXXXX-X)

### gatsby에 추가

yarn package site 에서 gatsby-plugin-google-analytics를 검색하고 설치합니다.
플러그인에 대한 전체 설명서는 [여기](https://www.gatsbyjs.org/packages/gatsby-plugin-google-analytics/) 에서 확인 가능합니다.

```
yarn add gatsby-plugin-google-analytics
```

기존 gatsby-starter-blog 에 이미 google analytics가 설치되어 있어서 버전업만 진행됩니다.

gatsby-config.js에 추적ID를 추가합니다.

```
`gatsby-plugin-sharp`,
    {
      resolve: `gatsby-plugin-google-analytics`,
      options: {
        trackingId: `UA-XXXXXXXXX-X`,
      },
    },
```

소스를 배포한후, analytics 사이트에 접속하여 정보를 확인합니다.
