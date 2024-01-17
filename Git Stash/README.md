# Git Stash

### 1. Git Stash
1. 설명 : commit된 특정 코드(=Staging에 존재)를 다른 작업 공간으로 이동 및 저장
2. 코드
   1) Stash 작업 공간 이동 : `$ git stash`
   2) Stash 작업 공간 확인 : `$ git stash list`
   3) Stash 메모 추가 : `$ git stash save '...'
   4) Stash 코드 불러오기 : `$ git stash pop` // Stack :: 가장 최근 것 불러옴
   5) 특정 Stash 삭제 : `$ git stash drop 0` // 0은 stash list 식별 번호
   6) 모든 Stash 삭제 : `$ git stash clear`
  
3. 왜 사용?
   1) 주석 사용 : Commit 할 때에도 반영되기 때문
   2) 기능 A, B 중 A를 먼저 작업하라고 할 때 : B를 Stash 공간에 보관하고 Merge 진행
   3) Git Branch 사용 : 용도가 비슷해서 취향껏 stash 사용
   
<br>
