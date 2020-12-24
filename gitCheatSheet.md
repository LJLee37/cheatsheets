# git Cheat sheet
## 초보자를 위한 순서
### 깃허브에서 생성할 때
* [깃허브 리포지토리 생성]()
* [깃허브에서 클론](#git-clone-normal)
### 기존 리포지토리를 깃허브에 올릴 때
* [새 리포지토리 생성](#git-init-local)
* [깃허브 리포지토리 생성]()
* [원격 저장소 설정]()
* [브랜치 게시]()
### 작업할 때
* [마스터로 체크아웃]() (최근의 깃허브에서는 메인이라는 이름을 사용한다.)
* [풀]()
* (선택적) [자신의 브랜치로 체크아웃]()
* [변경사항 스테이지]()
* [커밋]()
* [푸시]()
## 일반적인 순서

### git clone

#### git clone normal

원격 저장소의 리포지토리를 로컬로 처음 가져오는 작업.

```git clone 원격주소 [저장될 위치]```

원격 주소의 경우 주로 https://으로 시작하거나 git@으로 시작한다.

저장될 위치를 지정하면 해당 디렉터리 내부를 리포지토리로 사용한다. 지정하지 않으면 현재 working directory 밑에 리포지토리 이름으로 디렉터리를 만든 후 해당 디렉터리를 사용한다.

예를 들어 깃허브의 경우
> https://github.com/*Username*/*repository*

또는

> git@github.com:*Username*/*repository*

이다.

#### git clone options

* -l, --local
    * 원격이 로컬인 경우 사용한다. 
    * 하드링크를 시도한다.
* --no-hardlinks
* -s, --shared
    * 하드링크 대신 파일을 공유한다.
    * **위험!** 어지간하면 쓰지 말 것.
    * 써야 한다면 매뉴얼을 자세히 읽을 것.
* --bare
    * Bare 리포지토리를 만든다.
    * 원격 리포지토리용.
* --mirror
    * --bare을 내포한다.
    * 미러로 만든다.
* -o <이름>, --origin <이름>
    * origin 대신 주어진 이름을 사용한다.
* -b <이름>, --branch <이름>
    * 로컬 헤드를 원격 헤드와 같게 하는 대신 해당 브랜치로 한다.
    * checkout을 미리 하는 느낌.

##### 그 외

설명은 매뉴얼을 읽을 것.

* --depth \<depth\>

#### git url

* `ssh://[user@]host.addr[:port]/~[user]/path`
* `git://host.addr[:port]/~[user]/path`
* `http[s]://host.addr[:port]/path`
* `ftp[s]://host.addr[:port]/path`
* `[user@]host.addr:path` - ssh 사용함.

### git init

클론 없이 새로운 리포지토리를 생성하는 작업. 또는 원격 서버용도로 사용할 목적으로 사용할 수도 있다.

#### git init local

로컬에서 새로운 리포지토리를 생성하는 작업. 

```git init [리포지토리 이름]``` 

원격을 이용할 경우 직접 추가해야 한다. 

리포지토리 이름을 지정하지 않을 경우 현재 working directory를 리포지토리로 사용한다.

#### git init remote

원격으로 사용할 새로운 리포지토리를 생성하는 작업. 로컬로 사용할 수 없다.

```git init --bare [리포지토리 이름]```

### git remote

### git config

### git add

### git commit

### git push

### git pull

### git fetch

### git merge

### git reset

### git revert



