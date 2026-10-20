---
layout: post
title: "Example post title"
description: "One-line summary shown in the blog list and on share cards."
# image: /images/cover.png   # 공유 카드에 뜰 대표 이미지 (선택)
math: true                   # 수식이 있으면 true
---

_drafts/ 폴더의 글은 사이트에 공개되지 않아요. 이 파일을 복사해서
`_posts/2026-11-01-my-first-post.md` 처럼 날짜가 붙은 이름으로 `_posts/` 폴더에 넣으면 공개됩니다.

## Math

Inline math like $$p(y \mid x)$$ and display math (kramdown에서는 인라인 수식도 `$$...$$`로 감싸요):

$$
\mathcal{L}(\theta) = -\mathbb{E}_{(x,y)\sim\mathcal{D}}\left[\log p_\theta(y \mid x)\right]
$$

## Code

```python
def evaluate(model, loader):
    return sum(model(x).argmax(-1).eq(y).sum() for x, y in loader)
```

## Images

`images/` 폴더에 그림을 넣고 이렇게 참조해요:

![caption](/images/figure.png)
