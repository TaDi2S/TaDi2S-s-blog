---
# Front Matter
title: "minial-mistakes 관련 정리"
categories: blog
tags: jekyll, minial-mistakes, git page
date: YYYY-MM-DD HH:MM:SS +09:00

# 목차
toc: true  
toc_sticky: true 
---

# Minimal Mistakes 디렉토리 구조

> Minimal Mistakes 테마의 디렉토리 구조는 보통 다음과 같은 주요 폴더와 파일로 구성된다고 한다.

## _includes/:
- 여러 페이지에서 재사용될 수 있는 부분적인 HTML 템플릿 파일들을 포함.
- 헤더(header.html), 푸터(footer.html), 사이드바(sidebar.html) 같은 파일들이 위치.
- head.html, scripts.html, author-profile.html 등 중요한 구성 요소들이 포함되어 있어 페이지의 공통 레이아웃을 관리하는 데 사용.

## _layouts/:

- Jekyll의 레이아웃 파일이 저장되는 폴더로, 각 페이지의 기본 구조를 정의합니다.
- default.html: 기본 레이아웃 파일로, 대부분의 페이지가 이 레이아웃을 확장합니다.
- single.html: 블로그 게시물에 사용되는 레이아웃.
- home.html: 메인 페이지(홈 페이지)에 사용되는 레이아웃.
- archive.html: 아카이브 페이지에 사용되는 레이아웃으로, 블로그 포스트의 카테고리별 또는 태그별 목록을 표시합니다.

## _sass/:

- 이 폴더에는 SCSS(Sass) 파일들이 포함되어 있으며, 사이트의 스타일을 정의합니다.
- minimal-mistakes/: 이 하위 폴더에는 테마와 관련된 Sass 파티셜(partials)이 포함되어 있습니다. 예를 들어, _masthead.scss는 페이지 상단에 있는 헤더 섹션의 스타일을 정의합니다.
- custom.scss: 사용자가 정의한 Sass 스타일을 추가하여 테마 스타일을 덮어쓸 수 있는 파일입니다.

## assets/:

- 테마에 필요한 CSS, JavaScript, 이미지 등 정적 파일들이 포함됩니다.
- css/: 최종적으로 컴파일된 CSS 파일들이 위치합니다.
- js/: Jekyll 사이트에서 사용하는 JavaScript 파일들이 위치합니다. 예를 들어, main.js와 같은 사용자 정의 스크립트 파일이 여기에 있습니다.
- images/: 테마에서 사용하는 모든 이미지 파일들이 여기에 있습니다. 로고, 아이콘, 배경 이미지 등이 포함됩니다.

## _data/:

- YAML, JSON, CSV 형식의 데이터 파일을 저장하는 폴더입니다. 이 데이터는 Jekyll에서 사이트의 콘텐츠로 사용될 수 있습니다.
- authors.yml: 블로그의 여러 저자에 대한 정보가 포함됩니다.
- navigation.yml: 사이트의 네비게이션 메뉴를 정의하는 파일입니다.

## _posts/:

- 모든 블로그 포스트(markdown 파일)들이 이 폴더에 저장됩니다.
- 각 포스트 파일 이름은 YYYY-MM-DD-title.md 형식을 따릅니다.
- 이 폴더의 파일들은 블로그의 게시물로 사용되며, Jekyll은 이 파일들을 기반으로 블로그 포스트 페이지를 생성합니다.

## _config.yml:

- 사이트의 전역 설정을 정의하는 메인 구성 파일입니다. 예를 들어, 사이트의 타이틀, 설명, URL, 기본 언어, 네비게이션 메뉴, 플러그인, SEO 설정 등이 여기에 포함됩니다.

## index.html:

- 사이트의 기본 진입점이 되는 메인 인덱스 페이지 파일입니다.
- 일반적으로 홈 페이지의 구조와 콘텐츠를 정의합니다.

## Gemfile 및 Gemfile.lock:

- Ruby Gem을 관리하는 데 사용되는 파일들로, Jekyll 및 관련 플러그인들을 설치 및 관리합니다.
- Minimal Mistakes 테마를 설치하고 사용할 때 필요한 모든 Ruby Gem들을 나열합니다.

## 추가 구성 요소
- README.md: 테마에 대한 설명서 파일로, Minimal Mistakes 테마를 설치하고 설정하는 방법에 대한 지침이 포함되어 있습니다.
- LICENSE: 테마에 대한 라이선스 정보가 포함된 파일입니다.