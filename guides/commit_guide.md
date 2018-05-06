# SNUwagon commit/PR guide

### General

- Fork-PR 방식으로 협업하여주세요.
  - upstream repository에 푸시 권한은 있지만 바로 푸시하는 것은 권장하지 않습니다.
- 최신 버전을 유지하기 위해 PR이 머지된 후에는 upstream repository를 pull 해주세요.
  - git remote add upstream <upstream_repository>
  - git pull upstream master

- 이슈가 있을 때는 [backend repository](https://github.com/SNUWagon/SNUwagon-back)에 이슈를 먼저 올려주세요.
  - 제목에 [Backend] or [Frontend] 를 붙여서 확인하기 편하게 해주세요.
  - 이슈와 관한 커밋 메세지 or PR 에는 이슈 번호를 붙여주세요.
    - 백엔드에서는 #1 #2 등으로 붙일 수 있고,
    - 프론트에서는 SNUWagon/SNUwagon-back#1 꼴로 붙여주어야 합니다.

- CI 툴로 Travis CI를 사용합니다.
  - build fail일 시 PR이 거부됩니다.

- code coverage 툴로 codecov를 사용합니다.
  - coverage가 떨어지면 PR이 거부될 수 있습니다.

### Backend

- Python 3.5.2 버전을 권장합니다.
  - 그 외의 dependency는 requirements.txt 파일을 참고해주세요.

- PEP8 가이드라인을 따릅니다.
  - flake8을 사용하여 문법을 검사합니다.
  - README를 보고 pre-commit hook을 복사해주세요. 문법 오류 발생시 커밋을 막을 수 있습니다.


### Frontend

- Node 8.x 버전을 권장합니다.
  - 그 외의 dependency는 package.json 파일을 참고해주세요.

- ESLint를 사용하여 문법 검사를 합니다.
  - .eslintrc는 ARC에서 자동 생성된 것을 사용합니다.
  - README를 보고 pre-commit hook을 복사해주세요. 문법 오류 발생시 커밋을 막을 수 있습니다.
