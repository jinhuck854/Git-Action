# Add & Commit

### 1. Git init
1. 설명 : Git이 파일 및 폴더 로그 감시해줌
2. 코드 : `$ git init`
   
<br>

### 2. Add & Commit
/* 터미널 명령어로 Git 사용하는 방법 */

1. app.txt 파일 생성 후 저장 
2. Add 코드 : `$ git add app.txt`
3. Commit 코드 : `$ git commit -m '커밋 메시지'` 

<br>

### 2.1 UI 인터페이스로 Git 사용하는 방법
 
=> `VS Code 내장된 Git` 기능 사용
1. `Git UI` : Changes == git add, Staged Changes == git commit
2. `Git Graph 설치` 후 Git 창에서 그래프로 커밋 id, 설명, 날짜 등 알 수 있음

<br>

### 3. 그 외 유용한 용어 및 개념 정리
1. 작업 공간 <-> Staging Area <-> Repository Area
   1) 작업 공간 : 코드를 짜는 공간
   2) Staging Area : Commit 할 파일을 고르기 == add
   3) Repository Area : 저장소로 Commit

<br>

2. 파일 여러가지를 한 번에 Add & Commit
   1) `$ git add app.txt app2.txt ...`
   2) `$ git add.`

<br>

3. 깃 상태창 열기 (Status)
   1) 설명 : 어떤 파일이 Staging 또는 Commit 되었는지 알려줌
   2) 코드 : `$ git status`

<br>

4. 깃 Commit 내역 조회 (Log)
   1) 설명 : Commit 한 로그들 보여줌
   2) 코드 : `$ git log -all --oneline`
  
5. Commit 차이점 알기 (Diff)
   1) 설명 : Commit 하기 전, 이전 코드와 어떤 차이점이 있는지 확인하고 싶을 때
   2) 코드 : `$ git diff` 또는 ` $ git diff 커밋id1 커밋id2` 또는 `$ git difftool 커밋id1 커밋id2`

<br>


