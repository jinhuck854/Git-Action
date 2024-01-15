# Push & Clone & Pull

### 0. 원격 저장소 Branch 생성
1. 설명 : 기본 브랜치 생성
2. 코드
   1) Main Branch 생성 : `$ git branch -M main`
   2) Serve Branch 생성 : `$ git branch (branch 이름)`

### 1. Push
1. 설명 : 로컬 저장소 -> 원격 저장소 올릴 때
2. 코드
   1) 기본 : `$ git push -u (원격 저장소 주소) main`
   2) 변수 지정 : `$ git remote add (origin :: 변수명) (주소 :: https://...)
   3) 주소 기억 : `$ git push -u (주소) main`

      -> 이후에는 `$ git push`만 해도 해당 주소 기억함
3. !! Push 오류 !!
   1) 원인 : 원격 저장소와 로컬 저장소의 파일이 서로 다를 때 충돌(Conflict) 발생
   2) 해결 : `$ git pull`
<br>

### 2. Clone
1. 설명 : 원격 저장소 -> 로컬 저장소 내려받을 때
2. 코드 : `$ git clone (원격 저장소 주소)`

<br>

### 3. Pull
1. 설명 : 원격 저장소 -> 로컬 저장소 내려받을 때, `fetch + merge`

   // fetch : 원격저장소 신규 commit 가져옴
2. 코드
   1) 기본 : `$ git pull (원격 저장소 주소)`
   2) 변수 지정 : `$ git remote add (origin :: 변수명) (주소 :: https://...)
   3) 주소 기억 : `$ git push -u (주소) main`

3. Conflict 발생 가능하니 주의 바람

<br>
