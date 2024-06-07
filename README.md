- 출처 : https://github.com/hojihun5516/git_lecture
<br />

# Git 설명 목차 :pencil:

-----

0. [리눅스 계열 명령어 :art:](#0-리눅스계열-명령어-art)
   - ls 
   - cd
   - mkdir
   - vim

1. [Git과 GitHub의 차이:recycle:](#1-git과-github의-차이-recycle)
   - git
   - github
2. [Git 알아보기 :boom:](#2-git-알아보기-boom)
   - Git은 왜 만들어졌는가?
   - Git은 왜 쓰는가?
3. [Git 써보기 :hammer:](#3-git-써보기-hammer)
   - Git 설치 (Bash 깔림)
   - Git remote
   - Git add
   - Git commit
     - 첫 커밋일 경우 
       - git config --global user.email " "
       - git config --global user.name " "
   - Git ignore
   - Git checkout {branch}
   - Git merge
4. [GitHub 써보기:hammer_and_pick:](#4-github-써보기-hammer_and_pick)
   - GitHub는 뭔가요?
   - Git clone
   - Git push
   - Git pull
------
<br />

# 0. 리눅스계열 명령어 :art:

1. ### ls 

   - 현재 경로에 있는 파일들을 확인

2. ### cd

   - 원하는 경로의 폴더로 이동
   - ex) cd .. 
     - 한칸 뒤로이동
   - ex) cd {folder_name}
     - 같은 level에 있는 원하는 폴더로 이동

3. ### mkdir

   - 폴더 만들기
   - ex) mkdir my_folder

4. ### vim 

   - 파일 편집기 
   - vim a.txt
     - a.txt 생성 or 열기
   - 
   - 저장 안하고 나가는법   :q!
   - 저장하고 나가기         :wq

5. ### rm -rf 

   - 폴더 or 파일 삭제
   - ex) rm -rf node_modules -> node_modules라는 폴더 제거
   - 복구안되니까 신중하게 해주세요 ( 휴지통으로 안들어갑니다 )
<br />


# 1. Git과 GitHub의 차이 :recycle:

---

- ### Git

  - 버전관리 및 협업 도구

- ### GitHub

  - 서비스식 Git 저장소

<br />

# 2. Git 알아보기 :boom:

---

1. ### Git 은 왜 만들어졌는가?

   - Git이 없던 시절 분산버전 관리 시스템이라는 BitKeeper라는 시스템을 사용
   - 리눅스를 사용하던 개발자가 BitKeeper를 해킹하여 문제 발생
   - 리눅스 커널에서 더이상 무료로 BitKeeper를 사용하지 못함
   -  리눅스 오픈소스를 만든 리누스 토발즈가 개발
   - 소문에 의하면 2주만에 완성

2. ### Git은 왜 쓰는가?

   - 버전관리 가능
     - 기존의 압축파일 시스템의 문제점
     - 가벼운 메모리 차지
   - 협업 가능
     - 협업 시 같은 파일을 수정했을 경우 내용을 합치려면 일일이 다 확인해야하는 문제점을 해결

<br />

# 3. Git ​써보기 :hammer:

---

1. ### git 설치 

   - Bash 와 함께 설치
     - 리눅스 계열 운영체제에서 사용하는 쉘의 한 종류
     - 운영체제 커널과 사용자 사이를 이어주는 역할

2. ### git remote 

   - 편하게 url 주소라고 생각
   - ex) git remote add origin https://github.com/~~~~

3. ### git add => 깃에 변경된 파일기록을 쌓음

   - git add .  
     - 모든 파일 적재
   - git add {file_name}  
     - 특정 파일 적재
     - ex) git add a.txt

4. ### git commit => 기록들에 메시지 입력

   - git commit 
     -  커밋 메시지 Title과 Content 입력을 위해 vim으로 이동
   - git commit -m "제목"  

   - 첫 커밋일 경우 
     - git config --global user.email "이메일"
     - git config --global user.name "계정이름"
     - ex) git config --global user.email "abcd@naver.com"
   - commit 규칙
      	1. 제목과 본문을 빈행으로 분리
      	2. 제목 행을 50자로 제한
      	3. 제목 행 첫 글자는 대문자
      	4. 제목 행 끝에 마침표 넣지 않음
      	5. 제목 행에 명령문 사용
      	6. 본문을 72자 단위로 개행
      	7. 어떻게 보다는 무엇과 왜를 설명

5. ### git ignore => 깃의 관리를 받지 않을 파일 지정

   - .gitignore 
   - .git과 같은 level에 .gitignore 파일 생성

6. ### git checkout {branch} => 브런치 변경

   - Git checkout -b {branch} => 브런치 만들기
   - ex) git checkout -b temp => temp라는 브런치생성하여 temp로 이동
   - ex) git checkout master => 기존에 있던 master라는 브런치로 이동

7. ### git merge {branch}

   - 주체가 되길 원하는 브런치로 이동하여서 실행
   - ex) master에 temp브런치를 꽂고싶다면 master로 이동하여 git merge temp 실행
   - => 
   - 1) git merge temp
   - 2) merge conflict가 떴을때는 긴장하지말고 파일을 확인해봅니다
   - 3) 예제에서 HEAD~ ====가 master 
   - 4) HEAD ==== temp 지워주고 저장
   - 5) git add .
   - 6) git commit
   - 7) 끝

<br />

# 4. GitHub 써보기 :hammer_and_pick:

---

1. ### GitHub는 뭔가요?

   - 소스코드 호스팅서비스이자 소셜 코딩 플랫폼
   - 오픈소스들의 창구

2. ### Github 가입

3. ### git clone {url} => 원하는 레포지토리를 url을 이용하여 클론하여 내 로컬에 저장

   - ex) git clone https://github.com/~~~~

4. ### git push {remote} {branch} =>  여태 쌓은 branch의 commit들을 한방에 github에 호스팅

   - remote: origin을 이용하세요
   - origin: 나의 github 레포지토리 주소
   - branch: 올리고싶은 branch 이름
   - ex) git push origin master

5. ### git pull {remote} {branch} => 원하는 branch를 내려받아서 로컬의 해당 브런치에 자동 merge

   - ex) git pull origin master
