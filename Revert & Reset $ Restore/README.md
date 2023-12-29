# Revert & Reset & Restore

### 1. Revert
1. 설명 : 특정 commit에서의 작업 취소 후 다시 commit
2. 코드 : `$ git revert (커밋 id)`
   
   -> Vim 에디터가 뜰 수도 있는데, i눌러서 글자 수정하고 esc로 나올 수 있음. `:wq`로 저장
   
<br>

### 2. Reset // 잘 안 씀
1. 설명 : 특정 커밋이 생성될 때로 돌려줌
2. 유의사항 : 작업폴더 내 파일 모두 되돌아감
3. 코드
   1) `$ git reset --hard (커밋 id)` // 특정 커밋 id 이후의 모든 작업 삭제
   2) `$ git reset --soft (커밋 id)` // 특정 커밋 id만 삭제 후 특정 커밋 id는 staged area로 이동
   3) `$ git reset --mixed (커밋 id)` // 특정 커밋 id만 삭제

<br>

### 3. Restore
1. 설명 : 현재 파일의 가장 최근 commit된 상태로 되돌림 // Ctrl + z와 유사
2. 코드
   1) `$ git restore (파일명)`
   2) `$ git retore --source (커밋 id)`
   3) `$ git resotre --staged (파일명` // 잘 안 씀 
   
<br>
