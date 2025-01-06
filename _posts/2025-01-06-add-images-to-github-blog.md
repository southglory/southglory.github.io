---
layout: single
title:  "깃허브 블로그에 이미지를 추가하는 법"
---

깃허브 블로그에 이미지를 추가하는 방법은 여러 가지가 있습니다. 아래는 가장 일반적인 방법입니다.

### 1. 저장소에 이미지 업로드

1. 이미지 파일을 블로그 저장소에 업로드합니다.
   - 예: `assets/images/` 폴더에 `example.webp` 파일 추가.

2. 업로드한 이미지를 Markdown 문서에서 경로로 참조합니다.
   ```markdown
   ![EXAMPLE이라는 단어가 대문자로 중앙에 배치된 단순하고 깔끔한 이미지. 흰색 배경에 현대적인 굵은 산세리프 글꼴로 작성되어 있습니다.](assets/images/example.webp)
   ```
   
![EXAMPLE이라는 단어가 대문자로 중앙에 배치된 단순하고 깔끔한 이미지. 흰색 배경에 현대적인 굵은 산세리프 글꼴로 작성되어 있습니다.](assets/images/example.webp)


### 2. GitHub Issues를 활용한 이미지 추가

1. GitHub Issues에서 새로운 Issue를 작성합니다.
2. 이미지를 드래그하여 업로드하면 이미지 URL이 생성됩니다.
3. 생성된 URL을 복사하여 Markdown 문서에 삽입합니다.
   ```markdown
   ![이미지 설명](https://.../example.png)
   ```

### Alt Text 작성 가이드

이미지에 대한 **Alt text**(대체 텍스트)를 추가하여 접근성과 SEO를 향상시킬 수 있습니다. 

#### 작성 방법
- 간결하고 이미지의 내용을 설명하도록 작성합니다.

예:
```markdown
![골든 리트리버 강아지가 공을 가지고 노는 모습](assets/images/golden_dog_play_ball.webp)
```
![골든 리트리버 강아지가 공을 가지고 노는 모습](assets/images/golden_dog_play_ball.webp)

---

😊
