# Commitlint 적용을 위한 테스트 저장소

## Commitlint 란 무엇인가

Conventional Commits 검사 자동화 도구로 husky 를 이용해 githook 을 등록한다.

## Conventional Commits 란 무엇인가

명확한 커밋 히스토리를 생성하기 위한 간단한 커밋 컨벤션

1. 커밋 형식
    ```bash
    <type>[optional scope]: <description>

    [optional body]

    [optional footer(s)]
    ```
2. 커밋 종류 (Type)
    ```bash
    [
      'build',
      'chore',
      'ci',
      'docs',
      'feat',
      'fix',
      'perf',
      'refactor',
      'revert',
      'style',
      'test'
    ];
    ```

## 적용 방법

1. 원격 저장소에 파일 혹은 내용 추가
    ```
    ├── .husky
    |   └── commit-msg
    ├── .gitignore
    ├── package.json
    └── commit.config.js
    ```
2. [Node.js](https://nodejs.org/en) 설치
3. npx 설치
    ```
    npm install npx -g
    ```
4. 원격 저장소 복제
    ```
    git clone [원격 저장소 주소]
    ```
5. npm 의존성 설치
    ```
    npm install
    ```

## 결과

올바르지 않은 커밋 형식 사용 시 커밋이 거절되며 그 이유를 표시합니다.

![잘못된 커밋 예시](./docs/잘못된%20커밋%20예시.png)

## 참고

- [효율적인 커밋 메세지 관리를 위한 Conventional Commits 적용하기 | 블로그](https://blog.flynnpark.dev/13)
- [Conventional Commits | 공식 문서](https://www.conventionalcommits.org/ko/v1.0.0/)
- [husky | GitHub](https://github.com/typicode/husky)
