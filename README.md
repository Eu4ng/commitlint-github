# Template Commitlint

GitHub 저장소에 Commitlint 를 쉽고 빠르게 적용하기 위한 템플릿입니다.

## 사용 방법

아래 두 가지 방법 중 한 가지를 선택하여 사용하시면 됩니다.

### 템플릿으로 저장소 생성

1. `Use this template` 버튼 클릭 후 GitHub 저장소 생성
2.  `README.md` 삭제
3.  필요에 따라 `.gitignore` 을 수정하거나 새로운 `.gitignore` 에 아래 내용 추가

    ```
    # npm
    node_modules/
    package-lock.json
    */package-lock.json
    ```
5. git clone 후 npm 패키지 설치 (이 때 husky 는 자동으로 설치됩니다)

    ```sh
    npm i
    ```

### 저장소에 직접 추가

1. Release 된 `commitlint-github.zip` 파일 다운로드 후 압축 해제
2. GitHub 저장소의 루트 디렉토리에 붙여넣기
3.  필요에 따라 `.gitignore` 을 수정하거나 새로운 `.gitignore` 에 아래 내용 추가

    ```
    # npm
    node_modules/
    package-lock.json
    */package-lock.json
    ```
5. git clone 후 npm 패키지 설치 (이 때 husky 는 자동으로 설치됩니다)

    ```sh
    npm i
    ```

## Branch protection rule 권장 설정

![image](https://github.com/Eu4ng/template-commitlint/assets/59055049/ce306e72-ac22-47c5-a558-365b6bfc14e2)

## 결과

### 로컬 저장소

올바르지 않은 형식의 커밋 메시지 사용 시 커밋이 거절되며 그 이유를 표시합니다.

![image](https://github.com/Eu4ng/commitlint-github/assets/59055049/21de4744-82c1-4843-888e-10e5f60ca33e)

### GitHub 저장소

GitHub Action 을 통해 commitlint 검사가 이루어지며, 올바르지 않은 형식의 커밋 메시지가 포함된 경우 상태 검사가 실패 처리됩니다.
만약 Branch protection rule 에서 `Require status checks to pass before merging` 항목이 체크되어 있고, `Status checks that are required` 에 `commitlint` 가 추가되어 있는 경우에는 상태 검사 실패 시 병합 버튼이 비활성화됩니다.

![image](https://github.com/Eu4ng/commitlint-github/assets/59055049/46b407a8-78a9-44b4-9326-faf11af14351)

## 참고

- [효율적인 커밋 메세지 관리를 위한 Conventional Commits 적용하기 / 블로그](https://blog.flynnpark.dev/13)
- [Conventional Commits / 공식 문서](https://www.conventionalcommits.org/ko/v1.0.0/)
- [husky / GitHub](https://github.com/typicode/husky)
