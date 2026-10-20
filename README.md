# kh12043.github.io

Jon Barron 스타일 메인 페이지에 Jekyll 블로그를 붙인 구조입니다.
GitHub Pages가 Jekyll을 자동으로 빌드해 주므로 별도 설정 없이 push만 하면 배포됩니다.

## 처음 한 번만 하는 일

- 프로필 사진: `images/`에 사진을 넣고 `_config.yml`의 `photo:` 줄 주석을 풀어 주세요.
- 링크 추가(Google Scholar 등): `_config.yml`의 `links`에 한 줄씩 추가.

## 평소에 하는 일

| 하고 싶은 것 | 방법 |
| --- | --- |
| 블로그 글 쓰기 | `_drafts/example-post.md`를 복사해 `_posts/YYYY-MM-DD-제목.md`로 저장 (`_posts` 폴더가 없으면 새로 만들기) |
| 논문 추가 | `_data/publications.yml` 맨 위에 블록 하나 복사해 붙이기 |
| 링크 추가/수정 | `_config.yml`의 `links` |
| 이미지 | `images/` 폴더에 넣고 `/images/파일명`으로 참조 |

글 머리말(front matter)에서 쓸 수 있는 옵션:

```yaml
---
layout: post
title: "글 제목"
description: "한 줄 요약 (공유 카드와 블로그 목록에 표시)"
image: /images/대표이미지.jpg   # 공유 카드 이미지 (선택)
math: true                     # 수식 쓸 때만
---
```

## 자동으로 되는 것

- 첫 글을 올리면 메인 페이지에 "Blog posts" 섹션과 푸터의 Blog/RSS 링크가 자동으로 나타남 (`/blog/`에 전체 목록)
- `/feed.xml` RSS 피드
- 트위터/링크드인 공유 카드용 Open Graph 메타태그
- 다크 모드, 모바일 레이아웃
- 수식 (KaTeX): 글 머리말에 `math: true`를 넣고 `$$...$$`로 감싸요. 문단 안에 쓰면 인라인, 줄을 따로 쓰면 블록 수식이 돼요.

## 로컬에서 미리보기 (선택)

Ruby가 설치되어 있다면:

```bash
bundle install
bundle exec jekyll serve
# http://localhost:4000
```

## 커스텀 도메인 (선택)

도메인을 산 뒤 저장소 루트에 `CNAME` 파일을 만들고 도메인 한 줄(예: `yourname.com`)을 적습니다.
DNS에는 GitHub Pages IP로 A 레코드를 등록하고, `_config.yml`의 `url`도 바꿔 주세요.

## 예전 주소

템플릿을 바꾸면서 `/about/`, `/about.html`, `/cv/`는 메인 페이지로 이동하도록 해 뒀어요 (`about/`, `about.html`, `cv/`).
