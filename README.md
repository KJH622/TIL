# TIL

## 브랜치 정의
1. A branch is Git is simply a lightweight movable pointer to one of these commits.
    - 참고 : https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell
2. Git branches are effectively a pointer to a snapshot of your changes.
    - 참고 : https://www.atlassian.com/git/tutorials/using-branches

## 브랜치 합치기
- 이슈에 해당하는 작업을 수행할 때, 별도의 브랜치를 만들고 작업한다.
- 작업이 끝난 후에는, PULL REQUEST를 사용해 내가 작업한 브랜치를 중요 브랜치(`main`, `master`, `development`, `devel` 등)로 병합시켜야 한다.

### 명령어
- `git merge`
- 주의할 점 : `A`브랜치를 `B`브랜치로 합치려고 할 때는 `A`브랜치를 체크아웃 한 상태에서 `git merge B`를 입력한다.