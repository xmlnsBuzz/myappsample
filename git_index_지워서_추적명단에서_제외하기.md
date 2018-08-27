# 특정 파일을 .gitignore 파일목록에 지정했는데 계속 추적하는 경우 해결법

## 이유

.gitignore에 지정하기 전에 이미 git add 등의 명령으로 추적파일 목록에 등록되어 있기 때문이다. 그냥 진행해도 커밋이나 푸쉬등이 안 되지만, 헷갈리고 눈에 거슬릴 수 있으므로

>git rm --cached [파일이름]

[파일이름]과 같이 '[](대괄호)'로 묶인 부분은 입력시 대괄호까지 타이핑하는 것이 아니라 대괄호 속 내용만 입력한다. 

## 예

> git rm --cached index.html : index.html 만 해당.
> git rm --cached *.* : working directory의 모든 파일(들)이 해당.
> git rm --cached css/*.* : css 폴더의 모든 파일(들)이 해당.

으로 특정 파일을 지우거나

>git rm -r --cached Library/

명령으로 git의 추적파일목록(tracked file index)에서 통째로 삭제한다.