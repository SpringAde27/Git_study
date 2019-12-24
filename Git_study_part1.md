# Git_study_part1

-----------
## Part1. 로컬에 저장소 생성 & 저장소에 파일 생성 및 추가 & 원격지 전송

#### 1-1. git저장소로 사용할 프로젝트 폴더 생성 후 이동 - working  directory
```
$ cd d:
$ cd workspace
$ mkdir git_study
$ cd git_study
```  

#### 1-2. git저장소 초기화 (.git 파일 생성) - git으로 버전 관리
```
$ git init
```

#### 1-3. 텍스트 파일 만들기
```
$ vim hello.txt
```

#### 1-4. Staging Area에 파일 추가(commit할 파일 선택) - Add
```
$ git add hello.txt
// 한번에 추가하고 싶은 경우 
$ git add --all
$ git add .

// Staged >>> Modified : add 해제, Unstaged
$ git reset 파일명

// Modified >>> Unmodified : 수정한 파일을 되돌리기 (수정내용취소)
$ git checkout 파일명
```
 - `git status` : 파일 상태 확인
 - Tracked 상태
 - commit 대기상태

#### 1-5. 로컬 저장소에 저장 - commit
```
$ git commit -m "fitst commit"

// commit 취소 - modified, unstaged - 보존
$ git reset (--mixed) {commit number}
$ git reset HEAD~3 // 현재부터 3개 이전

// commit 취소 - staged - 보존
$ git reset --soft {commit number}

// commit 완전 취소 - unmodified - 삭제
$ git reset --hard {commit number}

// 기존 commit에 새로운 내용으로 commit 추가하여 덮어쓰기
$ git revert {commit number}
```
 - `git log (--oneline)` : commit 이력 확인
 - commit을 서버에 push한 상태라면 reset보다는 revert

#### 1-6. 로컬 저장소와 원격 저장소 연결 - remote
```
$ git remote add origin {url}
```
 - `git remote -v` : 원격 저장소 연결 확인

#### 1-7. 로컬 저장소의 내용을 원격 저장소에 보내기 - push
```
$ git push origin master
```
 - origin : 원격 저장소 별칭
 - master : 원격 저장소 브랜치
-----------