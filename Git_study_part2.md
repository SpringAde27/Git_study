# Git_study_part2

-----------
## Part2. Branch

#### 2-1. 브랜치 생성
```
$ git branch {브랜치 명}

// 브랜치 확인
$ git branch
```
 - `git checkout -b {브랜치 명}` : branch + checkout 동시에 수행
 - `git branch -d {브랜치 명}` : 브랜치 삭제

#### 2-2. 해당 브랜치로 이동
```
$ git checkout {브랜치 명}

// 브랜치에서 작업 후
$ git add {파일명}
$ git commit -m "{설명}"
```

#### 2-3. master 브랜치로 이동
```
$ git checkout master
```

#### 2-4. 브랜치 병합 - merge
```
// master브랜치로 이동했는지 확인!
$ git merge {작업 브랜치 명}
```

#### 2-5. 병합하면서 생기는 충돌 해결 - conflict
```
// 병합 실패한 파일에서 충돌이 발생한 부분을 수정 후
$ git add {파일명}
$ git commit -m "{ Conflict Resolved }"
```
 - `>>>>>>> HEAD` : 충돌 시작
 - `=======` : 어디 부분에 속해 있는지 경계 표시
 - `<<<<<<< {브랜치}` : 충돌 끝

#### 2-6. 브랜치 병합 - rebase
```
$ git checkout {작업 브랜치 명}
$ git rebase master // master를 기준으로 하여 브랜치를 앞으로 가져온다

// 병합 실패한 파일에서 충돌이 발생한 부분을 수정 후
$ git add {파일명}
$ git rebase --continue

// master와 작업 브랜치 병합
$ git checkout master
$ git merge {작업 브랜치 명}
```
-----------