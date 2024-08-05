# 스파로스 아카데미 Git 특강 실습 레파지토리
<img src="https://github.com/user-attachments/assets/b7bb897b-5a86-4ea8-9923-d402d44cac56" width="390" height="480" alt="Git 특강">

## 새로 알게된 내용
- log의 여러 옵션
- force-push, fast-foward 정의
  - origin에 있는 파일들을 local에서 수정 후 변경사항을 다시 push 할 때 종종 오류가 발생
  - force-push는 origin 커밋을 덮어쓰는 강제 푸쉬이므로 협업자의 origin의 커밋을 유실 시킬 수 있음
- fetch와 pull의 차이와 fetch를 사용하는 경우
  - fetch는 merge없이 최신 커밋을 가져오지 않으므로, 커밋하지 않고 로컬에서 변경사항 확인(테스트)이 가능함.  
- revert와 reset의 차이 및 reset 옵션의 차이
  - revert : 커밋 변경사항을 되돌리되 히스토리는 건드리지 않고 되돌린 기록을 새로운 커밋으로 남김
  - reset : 브랜치의 '커밋 포인터'를 이동
    -  `--hard` 옵션은 스테이징 영역과 워킹 디렉토리의 모든 변경 사항을 삭제하고, `--mixed`는 스테이징 영역만 초기화하며, `--soft`는 스테이징 영역에 변경 사항을 남기고 워킹 디렉토리는 유지함.
- switch와 rebase의 존재
  - switch는 checkout보다 좁은 의미로, 브랜치 이동의 경우 checkout 보다는 switch 쓰는 것을 권장
  - rebase를 통해 병합 커밋 없이 간결한 히스토리를 만들고, 최신 상태를 유지해 충돌을 줄일 수 있음
- pull request 절차

## 실습 내용

### 설정
- git config
- .gitignore 파일

### 확인 명령어
- git log
  - `--oneline`
  - `--graph`
  - `--stat`
- git status / diff
- git reflog

### 기본 명령어
- git clone
- git add 와 commit
- git push
- git pull 와 fetch

### 돌아가기
- git revert
- git reset
  - `--soft` / `--mixed` / `--hard`
 
### 브랜치 관련
- git branch
- git switch / checkout
  - git switch -c / -d / -D
  - git checkout HEAD^^^ == git checkout HEAD~3
- git rebase
  - `--continue`
  - `--abort`
- conflict 만들고 해결하기
- git cherry-pick
  
### GitHub
- Issue
- Pull Request
- fork

### 협업 방법론
- commit 컨벤션
- git flow : [2인 1조 실습](https://github.com/Baek-Seungyeop/git-pratice3)

### 기타
- git restore
- git clean
- git stash
