# InhouseMaker Public Pages

InhouseMaker 앱의 외부 공개용 최소 정적 페이지 세트입니다. GitHub Pages에 그대로 업로드하면 소개 페이지, 정책 페이지, Riot 검증용 `riot.txt`를 함께 공개할 수 있습니다.

현재 문서에는 운영자명 `황석범`, 문의 이메일 `tjrqja014@gmail.com`, 기준 날짜 `2026-04-15`가 반영되어 있습니다.

## 파일 구성

- `index.html`: 메인 공개 페이지
- `support.html`: 고객지원 페이지
- `privacy.html`: 개인정보처리방침
- `community.html`: 커뮤니티 가이드라인 / 운영정책
- `riot.txt`: Riot Developer Portal URL 검증용 파일
- `styles.css`: 공통 스타일

## GitHub Pages 배포 방법

1. GitHub에서 새 저장소를 만들거나 기존 저장소를 준비합니다.
2. 현재 파일들을 저장소 루트에 그대로 업로드합니다.
3. GitHub 저장소의 `Settings` > `Pages`로 이동합니다.
4. `Build and deployment`에서 `Source`를 `Deploy from a branch`로 선택합니다.
5. 배포 브랜치를 `main`으로, 폴더는 `/ (root)`로 선택합니다.
6. 저장 후 잠시 기다리면 GitHub Pages 주소가 발급됩니다.
7. 발급된 주소에서 `index.html`, `support.html`, `privacy.html`, `community.html`, `riot.txt`가 모두 열리는지 확인합니다.

## URL 예시

### 프로젝트 저장소인 경우

저장소 이름이 `InhouseMaker-legal`이고 GitHub 사용자명이 `example-user`라면:

- Product URL: `https://example-user.github.io/InhouseMaker-legal/`
- Support URL: `https://example-user.github.io/InhouseMaker-legal/support.html`
- Privacy Policy URL: `https://example-user.github.io/InhouseMaker-legal/privacy.html`
- Community Guidelines URL: `https://example-user.github.io/InhouseMaker-legal/community.html`
- Riot 검증 URL: `https://example-user.github.io/InhouseMaker-legal/riot.txt`

### 사용자/조직 페이지 저장소인 경우

저장소 이름이 `<github-username>.github.io` 형식이면 저장소명이 경로에 붙지 않습니다.

- Product URL: `https://example-user.github.io/`
- Support URL: `https://example-user.github.io/support.html`
- Privacy Policy URL: `https://example-user.github.io/privacy.html`
- Community Guidelines URL: `https://example-user.github.io/community.html`
- Riot 검증 URL: `https://example-user.github.io/riot.txt`

## Riot URL 검증 방법

`riot.txt` 파일은 반드시 저장소 루트에 있어야 합니다.

현재 파일 내용은 아래 한 줄입니다.

```txt
RIOT-VERIFY-CODE-PLACEHOLDER
```

실제 Riot 검증 코드를 받기 전까지는 이 값을 유지하세요. 코드를 받은 뒤에는 `riot.txt` 안의 한 줄만 실제 코드로 교체하면 됩니다.

예:

```txt
RIOT-VERIFY-REAL-CODE
```

검증 경로 예시:

- `https://<github-username>.github.io/<repo-name>/riot.txt`
- 사용자/조직 페이지 저장소라면 `https://<github-username>.github.io/riot.txt`

중요:

- `riot.txt` 안에는 검증 코드 한 줄만 넣습니다.
- 설명 문장, 공백 줄, 추가 텍스트를 넣지 않습니다.

## Product URL 제출 안내

Riot Developer Portal의 Product URL에는 메인 페이지 주소를 넣으면 됩니다.

예:

- `https://<github-username>.github.io/<repo-name>/`

정책 관련 URL은 각각 아래와 같이 제출할 수 있습니다.

- Support URL: `https://<github-username>.github.io/<repo-name>/support.html`
- Privacy Policy URL: `https://<github-username>.github.io/<repo-name>/privacy.html`
- Community Guidelines URL: `https://<github-username>.github.io/<repo-name>/community.html`

## 유지보수 포인트

- 모든 페이지는 상대경로 링크를 사용하므로 프로젝트 저장소와 사용자 저장소 모두에서 그대로 동작합니다.
- 별도의 빌드 도구, 패키지 매니저, 프레임워크가 필요하지 않습니다.
- 문안 수정은 각 HTML 파일과 `riot.txt`만 편집하면 됩니다.

## TODO

배포 전에 아래 항목만 최종 확인하거나 실제 값으로 교체하세요.

- `riot.txt`의 `RIOT-VERIFY-CODE-PLACEHOLDER`를 실제 Riot 검증 코드로 교체
- 실제 GitHub username 확인
- 실제 repo 이름 확인
- GitHub Pages 게시 후 실제 공개 URL 확인
