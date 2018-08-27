# Git 사용법

**이 문서의 한계**

이 내용은 git bash를 이용하는 방법이라서 각자의 컴퓨터에 [Git]이 설치되어 있고, 실습자가 최소한 간단한 HTML 문서를 만들 줄 안다는 전제하에서만 실습할 수 있다. 

이 실습의 목적은 git에 대한 최소한의 지식을 얻는 것이고, 실제로 실무 프로젝트를 수행한다면 Vscode의 git 기능을 사용하는 것이 편할 것이다.

## 예제에 사용하는 파일

1. dir1
    * app1.js
1. dir2
    * app2.js
1. index.html
1. main.css
1. main.js
1. readme.md (markdown 문서로써 이 설명이 담긴 문서다.)
1. .gitignore (git 관리에서 제외시킬 문서목록이 담기 파일.)
1. log.txt(제외시킬 파일.)

## 순서

- 해당 디렉터리를 탐색기로 열고 파일 창에서 우클릭하여 메뉴에서 git bash를 선택한다.

>_git init_

- git <span style="color:red;">_add_</span> 명령으로 추적할 파일을 추가(add)한다.

>_git add index.html_

- add 시킨 파일을 <span style="color:red;">'_rm --cached_ '</span>를  사용하여 추적(track)에서 제외시킨다. _**wildcard(asterisk) 문자를 사용할 수 있다.**_ 모든 파일을 add하려면 <br />('_**git add .**_')

**<span style="color:blue;">commit을 하기 위해서는 WD(Working Directory)의 문서 중 최소 1개 이상의 문서에 변경사항이 있어야 된다. WD 내에 변경된 문서가 없으면 commit해도 소용없다.</span>**

>_git rm --cached index.html_

- 모든 파일을 add 시킨다.

>_git add **.**_ *(모든 파일을 commit할 경우)*

>_git add **index.html**_ *(특정 파일을 commit할 경우의 예)*

- _git status_ 로 상태를 확인한다.

>_git status_

- 모든 파일을 commit 한다고 가정하고 _git commit_ 명령으로 vim editor로 들어간다.

>_git commit_

- Vim editor 상태

1. ' **i** '를 입력하여 insert mode로 들어간다.
1. commit할 문자를 입력한다. (commit할 문자란 github에 내가 어떤 내용을 커밋했는지 상기시키도록 해줄 내용이다.)
1. 입력이 끝나면 esc key를 눌러 insert mode에서 나온다.

1. **:wq** 를 입력하고 enter.
1. vim editor 상태에서 빠져 나온다.

- **<span style="color:green;">문서를 수정한 다음 '수정내용(commit message)'을 커밋할 경우</span>**


    - 특정 파일(예를 들어 index.html)을 커밋할 경우
    >_git add index.html_
    
    >_git commit -m 'changed index.html_

    <span style="color:green;">여기서 -m은 'message'란 의미고, 따옴표의 'changed index.html'은  커밋 메시지의 내용이다.</span>
<br><br>

- 특정 파일(예를 들어 index.html)을 커밋할 경우
    
>_git add index.html_
    
>_git commit -m 'changed index.html_

<span style="color:green;">여기서 -m은 'message'란 의미고, 따옴표의 'changed index.html'은  커밋 메시지의 내용이다.</span>

##<span style="color:green;">Git에서 관리하지 않을 문서를 지정(gitignore)하는 방법</span>

-------------------
이하는 작성중임.


- Git 관리에서 제외시킬 문서 목록은 '.gitignore 파일에 기록한다. .gitignore 파일을 열고 아래와 같이 'log.txt', 'dir2'(폴더) 를 입력한다.

>_log.txt_
>_dir2_

- add 명령으로 모든 문서를 추가해 본다. *.* 대신 아래와 같이 .(period)만 입력해도 된다.

>_git add &nbsp;**.**_

>_git branch login_

>_git commit -m 'Another changes'_

>_git chechout login(위에서 만든 login branch로 이동)_

>_touch login.html_

>_git add ._

>_git commit -m 'login form'_

>_git checkout login (login branch로 이동)_

<span style="color:green;"></span><span style="color:green;"></span>
