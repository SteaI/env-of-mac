상대적이면서도 절대적인 개인취향이 반영된
어떤 개발자의 맥 환경
==================
[blog.doortts.com](http://blog.doortts.com)

<br/>
# 1. 기본 설정들 변경

## dock 에서 불필요한 아이콘들 제거
안 쓰는 앱들은 Dock에서 지우자 (앱이 지워지는 건 아니니까 don't worry)

	독에서 지울 앱 아이콘에 마우스 오른쪽 버튼 -> options 
	-> 독에 유지하기(keep in dock) 선택해제


## 입맛에 맛게 트랙패드 조정
아.. 이 올드한 나의 입맛이란..

<img src='https://raw.github.com/doortts/env-of-mac/master/media/Trackpad_setting01.jpg'>

## Function key를 일반키로 설정
구식 개발자라 단축키 하나가 아쉬운 상황인지라..  볼륨 키우고 백라이트 조절 등이 필요 할때는 fn 키랑 조합으로 사용하면 되니까 무방. 
	
	설정 -> 키보드 -> 키보드 : '모든 F1, F2 등의  키를 표준 기능 키로 사용' 선택

## 화면 닫을때 암호물어보기 
안 그러면 내 정보는 공공재 된다.. (아.. 어차피 이미 늦었나.)

	설정 -> 보안 및 개인정보 -> 일반(General)

## 한영 키보드 전환을 빠르게

	설정 -> 키보드 -> 키보드단축키 - 좌측: 입력소스 
	-> '이전 입력소스 선택' 과 '입력 메뉴에서 다음 소스 선택' 단축키를 서로 교환함

## key hold시에 repeat이 동작하게 만들기(터미널 화면에서)

	defaults write -g ApplePressAndHoldEnabled -bool false 


## spotlight 단축키 변경
개인의 취향. 개발자 입장에서는 각종 기존 단축키들과 충돌나는게 아까워서.

	키보드 -> 키보드 단축키 -> spotlight 를 F12로 변경(show dashboard 는 uncheck)


## 잠금화면 메시지 설정
잠금화면에서 자신의 이름이나 이메일 등이 표시되도록. 분실시 찾아줄 수 있게
	
	설정 -> 보안 및 개인정보 -> 일반 -> 잠금 메시지 설정

## dashboard 사용안함으로 변경하기
위젯 안쓸꺼면 괜히 공간 및 자원만 쓰니까 없애자. 터미널창에서 아래 명령어 실행.

	defaults write com.apple.dashboard mcx-disabled -boolean YES 
	
	killall Dock 

## MAC에서 한글 마지막 글자 잘림현상 해결

	설정 -> 키보드(Keyborad) -> 글자(text) -> '자동으로 영문철자 수정' 해제


<br/>


## 컴퓨터 이름(Computer name) 바꾸기

설정 -> 공유 -> 컴퓨터 이름

# 2.자주 쓰는 도구들 설치

## appstore 에서 기존 구매 앱들 설치
이미 산거라도 쓸데 없는건 설치하지 않기!

- PopClip : text 선택시 이런저런 사용가능한 action 이 popup으로 뜸
- Yoink : 임시 스택 of everything
- Caffeine : 화면이 꺼지지 않게 유지
- Wunderlist : 할일 관리
- Monosnap : 캡처도구

## BTT (Better Touch Tools) 설치
[http://blog.boastr.net/](http://blog.boastr.net/)

	three finger swipe up/down -> command + up/down 으로 설정

## Asepsis 설치 
mac에서 finder로 이동시 만들어지는 .DS_Store파일 생성을 막아준다

[http://asepsis.binaryage.com](http://asepsis.binaryage.com)


## Evernote 설치
[https://evernote.com/](https://evernote.com/)

## MS intellipoint 설치 
why? MS 마우스 사용자들에게 감도를 높여줌
	설정 -> Microsoft Mouse -> pointer options -> IntelliPoint pointer Speed

## sublime text 3 설치
[http://www.sublimetext.com/3](http://www.sublimetext.com/2)

TextMate를 오픈소스화 시킬 정도의 파급력을 가진 최고의 에디팅 툴

## chrome 설치
워낙 extention들이 좋은게 많아서.. 

추천 extention
- CrxMouse : Mac 크롬을 지원하는 마우스 제스처
- TweetDeck : twitter와 facebook을 동시에 지원
- Vimium : h,j,k,l
- Neater Bookmarks : 내 bookmark 간단 검색

[https://www.google.com/intl/en/chrome/browser/](https://www.google.com/intl/en/chrome/browser/)

## brew 설치 
Mac용 Command installer. 앞으로는 커맨드로 왠만한 도구들을 설치

	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

## XCode Command Line Tools 설치가 필요하다면(gcc 컴파일러 들어 있음)
XCode를 설치해도 되지만 XCode 안쓰는데도 2기가 짜리를 설치할 필요가 없으니 gcc/git 등의 command tool만 설치!

  [https://developer.apple.com/downloads](https://developer.apple.com/downloads/index.action#)

### brew를 통해	 git 설치

	brew git install

참고: [http://mxcl.github.io/homebrew/](http://mxcl.github.io/homebrew/)

## Karabiner 설치
why? 오른쪽 command를 한영전환으로 변경. 키 반복입력을 빠르게 만들기.

다운로드:	 [https://pqrs.org/osx/karabiner/](https://pqrs.org/osx/karabiner/)

	change command_r to command_r, send Delete를 해제하고
	change command_r to command_r, 'when you type command_r only send command + space' 를 선택

	Key repeat에서 wait 타임을 83 -> 30으로 변경

## Seil: caps lock 을 ctrl 키로 변경 (left control:: 59)
https://pqrs.org/osx/karabiner/seil.html.en 

## TotalFinder 설치 (유료)
Mac의 이상?불편?한 finder를 개선시켜줌

[http://totalfinder.binaryage.com](http://totalfinder.binaryage.com)


## dropbox 설치
[www.dropbox.com](https://www.dropbox.com/)

## Alfred 설치
App Launcher (no gomin, go install)

[http://www.alfredapp.com/](http://www.alfredapp.com/)

## Bartender 설치 (유료)
메뉴바 아이콘이 길어지는 걸 해결
http://www.macbartender.com

## iterm2 설치
기본 터미널보다 우수함. 

[http://www.iterm2.com/](http://www.iterm2.com/)

대체제: http://tmux.sourceforge.net/

## oh my zsh 설치
shell이라면 zsh !! bash 안녕~! (but 저사양 맥북에서는 때때로 느려질때도..)

	curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh

참고: [https://github.com/robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

### zsh command syntax highlighting 만들기
	
[https://github.com/zsh-users/zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)


## appcleaner 설치
설치된 앱을 깨끗하게 지우자

[freemacsoft.net/appcleaner](http://www.freemacsoft.net/appcleaner/)

## mouse wheel 만 natrual scroll 에서 제외시키기

karabinar 이용하면

- General > Don't remap Apple's pointing devices
- Pointing Device > Reverse scrolling direction > Reverse Vertical Scrolling

## Developer Color Picker 설치
개발자용 컬러 피커. 색을 다루는 개발자라면!

[http://panic.com/~wade/picker/](http://panic.com/~wade/picker/)

## go2shell 설치 후 설정 (mac appstore)
finder에서 현재 폴더로 터미널 띄우기
http://zipzapmac.com/go2shell


# for Unix Shell

## autojump
Rank 기반 디렉터리 이동
https://github.com/joelthelion/autojump

## vim related
https://github.com/bling/vim-airline

## git diff highlight

curl https://raw.githubusercontent.com/git/git/master/contrib/diff-highlight/diff-highlight > /usr/local/bin/diff-highlight && chmod +x /usr/local/bin/diff-highlight

## git config 
```
alias.co=checkout
alias.edit=!f() { git diff --name-status --diff-filter=U | cut -f2 ; }; vi `f`
alias.add-unmerged=!f() { git diff --name-status --diff-filter=U | cut -f2 ; }; git add `f`

pager.log=diff-highlight | less -F -X
pager.show=diff-highlight | less -F -X
pager.diff=diff-highlight | less -F -X

rerere.enabled=true

pull.rebase=true
credential.helper=cache --timeout=604800

```
