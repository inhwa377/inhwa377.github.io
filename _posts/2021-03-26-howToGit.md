---
title: Git 사용법
categories: [Git]
comments: true
---

<dfn info="분산형 버전 관리 시스템(VCS)">Git</dfn>을 사용하는 방식은 3가지가 있다. <br>

1. SourceTree라는 Git GUI툴을 이용
2. Git GUI 자체 툴
3. Git Bash

나는 3번 Bash를 이용해서 Git을 사용하려 한다.<br>
<br>

## 기본 사용법

<br>
<p>화면 초기화 : Ctrl + L </p>
<p>한 행의 처음과 끝 : Ctrl + A, Ctrl + E </p>
<p>목록 보기 : ls 또는 dir </p>
<p>파일의 내용 보기 : cat </p>
<p>특정 문자를 검색 : grep </p>
<p>디렉터리로 이동 : cd </p>
<p>디렉터리 생성 : mkdir </p>
<p>파일 삭제 : rm </p>
<p>파일 생성 : touch </p>
<p>해당 명령어 빠져나오기 : q </p>
<br><br>

## git add? commit?

Git의 Repository 구조는 크게 세가지로 구성되어 있다.<br>
<br>
작업폴더(Working directory) > 인덱스(Staging Area) > 저장소(Head -Repository) <br>
<br>
우리가 작업하는 폴더를 작업트리(Working directory) 라고 부르며 commit을 실행하기 전에 작업트리와 저장소 사이에 존재하는 가상의 준비 영역(Staging Area)을 인덱스(Index)라고 한다.<br>
git add는 작업 디렉토리(working directory) 상의 변경 내용을 스테이징 영역(staging area)에 추가하기 위해서 사용하는 Git 명령어이다.<br>
git commit은 스테이징 영역(staging area)에 있는 내용을 저장소(Repository)에 올리기 위한 Git 명령어이다.
<br><br>

## git config

git bash를 쓴다면 보통은 처음에 잡아주는 설정이다.<br>

```
// git commit에 사용될 username
git config --global user.name "your_name"
 
// git commit에 사용될 email
git config --global user.email "your_email@example.com"
 
// 설정한 내용을 확인할 수 있다.
git config --list

```
<br><br>

## git init

현재 디렉토리를 기본 저장소로 설정한다.<br>

```
// 로컬저장소로 설정할 프로젝트 위치로 이동한다.
cd D:/Git
 
// 로컬저장소로 설정한다.
// (master) 브랜치로 보이면 성공한 것이다.
git init
 
// 만약 init을 취소하려면 아래의 명령어를 입력한다.
rm -r .git

```
<br><br>

## git status

```
//로컬 저장소의 현재 상태를 보여준다.
git status

```
<br><br>

## git add

파일을 준비영역(Staging Area)으로 옮긴다. (GitHub와 연동하려면 git remote로 원격 저장소와 연결해야 함)<br>

```
// a.html 파일만 추가
git add a.html
 
// 워킹 디렉터리 내 모든 파일을 추가
git add .
 
// 명령 프롬프트에서 상호작용하면서 추가 (나갈땐 q를 입력)
git add -i
 
// 진행중인 파일일 경우, Staging Area에서 워킹 디렉터리로 옮겨온다. 
$git rm --cached a.html
$git rm -r --cached .
```
<br><br>

## git commit

```
// 에디터가 출력되고, 에디터에서 커밋 메시지 입력 후 저장하면 커밋됨
git commit
 
// 간단한 커밋 메시지를 입력후 커밋
git commit -m "커밋 메시지"
 
// Staging Area에 들어간 파일에 대해서만 (워킹 디렉터리는 적용 X)
git commit -a -m "커밋 메시지"

```
<br><br>

## git log

```
// 커밋 이력 상세조회
git log 
 
// 커밋 이력중 커밋ID, 타이틀 메시지만 조회
git log --oneline
 
// 모든 브랜치 커밋 이력 조회
git log --oneline --decorate --graph --all
 
// 특정 파일의 변경 커밋 조회
git log -- a.html

```
<br><br>

## git remote

```
// Github 원격저장소와 연결한다.
git remote add origin [자신의 Github 원격저장소 주소]
 
// 연결된 원격저장소 확인한다.
git remote -v

```
<br><br>

## git push
```
// 원격저장소에 저장한다.
git push -u origin master
 
// 에러 - ! [rejected] master -> master (fetch first)
// 이미 변경된 파일이 원격저장소에 있을경우 발생
git pull origin master 
 
// 에러 - ! [rejected] master -> master (non-fast-forward)
git push origin +master

```
<br><br>

## git diff

작업폴더(Working directory)와 다른 커밋을 비교한다.<br>

```
// 현재 브랜치의 마지막 커밋과의 차이점 비교
$git diff

// 특정 커밋과의 차이점 비교
$git diff [Commit ID]

// 특정 커밋과 특정 파일의 차이점 비교
$git diff [Commit ID] -- [파일 경로]

```
<br><br>

## git branch

브랜치를 생성,수정,삭제 한다<br>

```
// 브랜치 보기
git branch

// 브랜치 생성
git branch [브랜치명]

// 브랜치 수정
git branch -m [브랜치명] [바꿀이름]

// 브랜치 삭제
git branch -d [브랜치명]

```
<br><br>

## git checkout

워킹 디렉터리의 소스를 특정 커밋 또는 특정 브랜치로 변경한다.<br>

```
// 특정 브랜치로 워킹 디렉터리 변경
$git checkout [브랜치명]

// 특정 커밋으로 워킹 디렉터리 변경
$git checkout [Commit ID]

// 특정 파일을 해당 브랜치 또는 커밋 상태로 변경 (원복)
$git checkout [돌아갈 Commit ID] -- [파일 경로]
*충돌 방지를 위해 브랜치명을 확인하고, 파일 추가 및 수정한 뒤 커밋해야 한다.

// 브랜치 생성 및 체크아웃을 같이 할 경우
$git checkout -b develop

```
<br><br>

## git merge

두 브랜치를 병합한다<br>
같은 파일의 같은 위치의 내용이 변경된 경우 충돌이 발생한다.<br>

```
git checkout master

git merge develop

```
