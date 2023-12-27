# Branch & Switch

### 1. Branch
1. 설명 : Main에서 작업하기에는 실패/충돌 부담이 클 때 `복제본 생성 후 작업`
2. Branch 코드 : `$ git branch (이름)`
   
<br>

### 2. Switch
1. 설명 : Branch 생성 후 이동할 때 쓰는 명령어
2. 코드
   1) Main to Branch : `$ git switch (branch 이름)`
   2) Branch to Main : `$ git switch main`
   3) Branch 로그 확인 : `$ git log --all --oneline --graph`

<br>

### 3. Merge // 협업할 때에 가장 중요함
1. 설명 : Branch에서 작성한 기능 및 코드가 잘 동작할 때에 Main에 병합하는 작업
2. 코드 : `$ git merge (branch 이름)`
   
   -> `Conflict 오류 발생` 가능 주의

   -> !! Merge 이후 Branch 공간은 그대로 남아있음을 유의 !!
   
<br>

### 3.1 다양한 Merge 방법
1. `3-way Merge`
   1) 설명 : Main과 Branch 모두 Commit이 존재할 경우 Main에서 Merge하는 방법, 중요 기능에서 주로 쓰임 // Default Merge 방법
   2) 코드
      1) `$ git switch main`
      2) `$ git merge (branch 이름)` // Main에서 코드 입력
      3) `$ git commit -m '커밋 메시지 내용'`
   4) 단점 : git log를 확인할 때에 모든 branch 선이 보이기 때문에 시각적으로 보기 힘들다
   5) 해결 : Rebase 또는 Squash Merge 방법 사용
  
2. `Fast-forward Merge`
   1) 설명 : Main에서 Commit(변동사항) 없을 경우 Branch를 Main으로 지정하는 방법
   2) 코드
      1) `$ git switch main`
      2) `$ git merge (branch 이름) // Main에서 Commit 없으면 자동으로 실행?
      3) `$ git commit -m '커밋 메시지 내용'`

3. `Rebase Merge`
   1) 설명 : Branch를 나눈 Main의 시점을 최근 Main으로 이동시킨 후 Fast-Forward Merge 방법 사용
   2) 코드
      1) `$ git switch (branch 이름)`
      2) `$ git rebase main` // Branch에서 코드 입력
      3) `$ git commit -m '커밋 메시지 내용'`
   4) 단점 : 브랜치끼리 차이가 많은 경우 충돌(Conflict) 많이 발생함
    
4. `Squash Merge`
   1) 설명 : Branch의 Commit 내용들을 떼와서 Main에 붙이고 새로운 Commit 함
   2) 코드
      1) `$ git switch main`
      2) `$ git merge --squash (branch 이름)` // branch 커밋 내용을 main으로 가져옴
      3) `$ git commit -m '커밋 메시지 내용'` // main에서 새로운 commit 함
    
<br>

### 3.2 Merge 이후 Branch 삭제
1. Merge 완료된 Branch 삭제 코드
   `$ git branch -d (branch 이름)`

2. Merge 안 한 Branch 삭제 코드
   `$ git branch -D (branch 이름)`

<br>

### 4. Conflict
1. 설명 : Branch와 Main에서 작업한 코드 라인이 동일할 경우 어느 것이 수정된 작업인지 몰라서 발생하는 오류
2. 해결 방법
   1) 충돌한 Main 또는 Branch에서 코드 수정
   2) git add .
   3) git commit -m 'comflict 해결 완료' // 오류 메시지 자유롭게 작성

<br>
