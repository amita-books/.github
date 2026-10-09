# amita-books/.github

Amita Books Organization의 공통 저장소입니다. `profile/README.md`가 Organization 첫 화면에 표시됩니다.

## 구성

| 경로 | 내용 |
|------|------|
| `profile/README.md` | Organization 첫 화면 (책 목록) |
| `assets/amita-books-avatar.png` | Organization 프로필 이미지 (1000×1000) |
| `assets/book-*-social.png` | 각 책 저장소의 소개 이미지 (Social preview, 1280×640) |
| `assets/src/*.html` | 위 이미지의 원본. 브라우저로 그려 PNG로 저장한다 |

## 이미지 다시 만들기

원본 HTML을 Chrome 헤드리스로 화면 크기 그대로 캡처한다 (macOS 예).

```bash
CHROME="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
"$CHROME" --headless=new --hide-scrollbars --window-size=1000,1000 \
  --screenshot=assets/amita-books-avatar.png "file://$PWD/assets/src/avatar.html"
"$CHROME" --headless=new --hide-scrollbars --window-size=1280,640 \
  --screenshot=assets/book-legacy-spring-board-social.png \
  "file://$PWD/assets/src/book-legacy-spring-board-social.html"
```

글꼴: Didot, Bodoni 72(macOS 내장), 나눔명조·나눔고딕. 다른 운영체제에서는 글꼴이 바뀌어 모양이 달라진다. macOS 내장 글꼴은 각 글꼴의
라이선스를 따른다.

새 책을 내면 소개 이미지 원본을 복사해 오른쪽 글자(권 번호, 제목, 스택, 소개)만 바꾸고, `profile/README.md`의 책 목록에 한 줄을 더한다.
