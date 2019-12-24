# Git_study_part3

-----------
## Part3. Life Cycle of File

#### 3-1. working  directory의 파일들은 Tracked / Untracked 상태를 가진다.
```
Tracked파일은 이미 스냅샷에 포함돼 있던 파일로 3가지 상태를 가진다.
	- Unmodified : 마지막 commit 이후 아무것도 수정되지 않은 상태
	- Modified : 파일이 수정된 상태
	- Staged : 수정한 파일을 add한 상태, commit대기 상태
```
 - `git reset {파일명}` : Staged → Modified(Unstaged) : add 해제
 - `git checkout {파일명}` : Modified → Unmodified : 수정한 파일을 되돌리기 (수정내용취소)
 - `git reset {파일명} + git checkout {파일명}` : Staged → Modified → Unmodified
 - commit을 서버에 push한 상태라면 reset보다는 revert
-----------