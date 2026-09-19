# my-app

Cloudflare Pages에 배포할 수 있는 가장 기본적인 정적 웹 앱입니다. 화면에는 제목 **Hello World!**와 소개 문구 **I'm Junhyuk Choi**를 표시합니다.

프레임워크와 빌드 도구를 사용하지 않으므로 파일을 수정한 뒤 바로 결과를 확인하고 배포할 수 있습니다.

## 파일 구성

```
public/
├── index.html    # 페이지 구조와 표시할 문구
└── styles.css    # 화면 디자인과 반응형 레이아웃
```

## 로컬에서 확인하기

`public/index.html` 파일을 브라우저에서 열면 됩니다. 간단한 정적 페이지이므로 설치하거나 빌드할 도구가 없습니다.

## 문구와 디자인 변경하기

- 제목 또는 소개 문구: `public/index.html` 안의 `h1`, `p` 텍스트를 수정합니다.
- 색상, 글꼴, 여백: `public/styles.css`의 맨 위 `:root` 색상 변수와 각 스타일 규칙을 수정합니다.
- 코드 안에는 각 영역이 담당하는 일을 설명하는 주석이 있어, 필요한 부분을 찾기 쉽습니다.

## Cloudflare Pages 배포

GitHub에 이 프로젝트를 올린 후 Cloudflare 대시보드에서 다음처럼 설정합니다.

1. **Workers & Pages**에서 **Create application** → **Pages** → **Connect to Git**을 선택합니다.
2. `jhchoi1021/my-app` 저장소를 연결합니다.
3. 배포 설정에서 다음 값을 사용합니다.
   - Framework preset: `None`
   - Build command: 비워 둠
   - Build output directory: `public`
4. **Save and Deploy**를 누릅니다.

이후 `main` 브랜치에 변경 사항을 푸시하면 Cloudflare Pages가 자동으로 새 버전을 배포합니다. 다른 브랜치로 올린 변경 사항은 미리보기 배포로 확인할 수 있습니다.

## 현재 상태

이 작업본은 로컬에만 있습니다. 아직 커밋하거나 GitHub에 푸시하지 않았고, Cloudflare Pages에도 배포하지 않았습니다.
