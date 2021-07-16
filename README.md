# Git

(버전)코드 관리 도구



# SCM & VCS & DVCS

- SCM : Source Code Mangaement(소스 코드 관리)
- VCS : Version Control System(버전 관리 시스템)
- DVCS : Distributed Version Control System(분산형 버전 관리 시스템) 



# Git 3대 기능

- Version 버전관리
  - 변경 이력 트랙킹
  - 언제든지 특정 시점으로 이동 가능
- Backup 백업
  - 최소 2대의 컴퓨터
  - Local Repository, Remote Repository
- Collaborate 협업



## Git 버전관리(Version)

> Git은 **폴더 단위**로 코드를 관리

### `git init` : Initialize repository

특정 폴더를 git으로 관리 시작

- `(master)` 프롬프트에 표시
- `.git` 폴더 생성 (git repository)
  - `.git` 폴더 삭제 시 git 관리 중지  `rm -r .git`

```
$ git init
Initialized empty Git repository in C:/Users/Kimmy/recap/.git/
```





### `git config`

설정

- `git config [설정할내용] [설정한 값]`
  - `git config user.name '이름'`
  - `git config user.email '이메일'`
  - `git config --global`: 전역 설정

```
Author identity unknown: 작자 미상

*** Please tell me who you are.: 니가 누군지 말해주세요.

Run 다음을 실행하세요

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
to set your account's default identity.
Omit --global to set the identity only in this repository
```





### `git stauts` : working tree status

git에게 상태 확인

- `git init`직후

```
On branch master: master라고 하는 branch에 있어

No commits yet: 아직 commit 없어

nothing to commit (create/copy files and use "git add" to track)
: commit 할 게 없어 (트래킹 하고 싶으면 `git add` 명령어를 사용해)
```

- `a.txt` 파일 생성 직후

```
Untracked files: 추적되지 않은 파일이 있어
	(use "git add <file>..." to include in what will be committed)
		a.txt (빨강)
	commit 될 수 있게 포함하고 싶으면 `git add <파일명>`을 사용해
	
nothing added to commit but untracked files present (use "git add" to track)
```



### `git add [파일명]` : add to staging area

Staging Area(스냅샷 무대)에 파일 추가



### `git commit -m "커밋 메시지"` : create version

버전을 생성

- 커밋(버전) 구성 요소
  - hash(해시)
  - 작성자
  - 날짜
  - 커밋메시지: 버전에 대해 설명

```
[master (root-commit) c244c22] First commit
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 a.txt
```



### `git commit -am "커밋 메시지"`

add와 commt -m 한번에 하는 명령어



### `git log` : show version

버전(커밋)들의 히스토리(로그)



### `git checkout `

`git checkout []` 특정시점으로 이동

`git checkout master` 최신 시점으로 이동



###  `git diff [파일명]`

`git diff [파일명]` 버전 전 후의 차이 점을 보여준다





## Git 백업(Backbup)

> 최소 2대의 컴퓨터 지역저장소(Local Repository), 원격저장소(Remote Repository), 클론저장소(Clon Repository)
>
> Local Repository<-------Pull<------- Remote Repository
>
> Local Repository------->Push------- >Remote Repository

1. 원격 저장소 생성
2. remote 정보 입력
3. git push



### `git hosting`

`GitHub` : 오픈소스의 성지

`gitLab.com` : 



###  `git remote` 원격저장소 명령어

- `git remove -v`  : 상세출력 (v = verbose)

- `git remote add`
  - `git remote add` [저장소 별명] [저장소 주소]
    - `git remote add [origin]`[ https://github.com/MinYongKim/first.git]



### `git push`

원격 저장소에 코드 백업

- `git push [저장소 별명] [브랜치 이름]`
  - `git push origin master`



### `git 복제`(Clone)

git clone https://github.com/MinYongKim/first.git



### `git Pull`







## 협업(Collaborate)

