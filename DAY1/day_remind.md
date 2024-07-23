# Git 과 Github

## [1] Git이란?
- (분산) 버전 관리 프로그램

## [2] Git 시작하기
1) 누가 어떠한 변경사항을 남겼는지, git이 자동으로 만들어 주기 위해서 필요하다!
global 한 정보를 주었기 때문에 "최초" 한 번만 설정하면 됨.

```
(1) git config --global user.name "이름"
(2) git confog --global user.email "메일 주소"
```

확인하기 위해서는
```
git config --global --list
```

## [3] Git의 3공간
1. working directory -> 분장실
2. staging area -> 무대
3. repository -> 사진 저장소

분장실 -> 무대 -> 사진 저장소로 우리가 사진을 찍어 내기 위해서 기본 명령어 사용함


## [4] Git 기본 명령어
### (1) git init
로컬 저장소를 만든다 -> 현재 작업 중인 디렉토리를 Git으로 관리한다.

```
git init
```

이후, '(master)' 표시가 뜨게 된다.

### (2) git add
working directory에서 작업이 완료된 파일을 무대(stage area) 위로 올린다.

```
git add 파일명
```

### (3) git commit 
staging area 즉, 무대 위에 있는 모델의 사진을 찍는다. 기록한다.

```
git commit -m"변경사항이 기록된 이유"
```
> 메세지(-m)를 남기는 이유?
버전 관리 프로그램 git이 자동으로 변경사항에 대한 "육하원칙"을 작성하기 위해 왜 바꾸었는지에 대한 정보가 필요해서

### (4) git status
각 파일들의 상태를 알려줌(Untracted, modified, New file...)

```
git status
```

### (5) git log
변경사항들의 기록을 보여줌

```
git log --oneline
```

==> 로컬 저장소(내 컴퓨터에서 버전 관리하기)


## Github
서버컴퓨터처럼 원격에서 나의 변경사항 기록들을 가지고 있도록 사용할 수 있다.

### (1) repository 생성
1. 우측 상단 + 버튼을 눌러서, repository 만든다.
2. URL 생성된다 -> 원격 저장소의 주소를 의미한다.
3. 복사

### (2) 로컬 저장소와 연결
```
# 원격 저장소 연결
git remote add origin URL

# 원격 저장소 연결을 확인
git remote -v
```

### (3) 변경 사항을 로컬 저장소에서 원격 저장소로 보내기
로컬 저장소와 커밋을 원격 저장소에 반영
```
git push origin master
```