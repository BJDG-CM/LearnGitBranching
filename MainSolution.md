#1 git 기본

##1.1 Git 커밋 소개

git commit
git commit

##1.2 Git에서 브랜치 쓰기

git branch bugFix
git checkout bugFix

##1.3 Git에서 브랜치 합치기(Merge)

git checkout -b bugFix    
git commit  
git checkout main
git commit
git merge bugFix

##1.4 리베이스(rebase)의 기본

git checkout -b bugFix    
git commit    
git checkout main    
git commit    
git checkout bugFix    
git rebase main

#2 다음 단계로

##2.1 HEAD 분리하기

git checkout C4

##2.2 상대 참조 (^) (Relative Refs)

git checkout C4^

##2.3 상대 참조 #2 (~)

git branch -f main C6
git branch -f bugFix C0
git checkout C1

##2.4 Git에서 작업 되돌리기

git reset local~1
git checkout pushed
git revert pushed

#3 코드 이리저리 옮겨다니기

##3.1 Cherry-pick 소개

git cherry-pick C3 C4 C7

##3.2 인터랙티브 리베이스 소개

git rebase -i HEAD~4

#4 종합선물세트

##4.1 딱 한 개의 커밋만 가져오기

git checkout main
git cherry-pick C4

##4.2 커밋들 갖고 놀기

git rebase -i HEAD~2
git commit --amend
git rebase -i HEAD~2
git branch -f main HEAD

##4.3 커밋 갖고 놀기 2

git checkout main
git cherry-pick C2
git commit --amend
git cherry-pick C3

##4.4 Git 태그

git tag v0 C1
git tag v1 C2
git checkout v1

##4.5 Git 설명

git commit

#5 고급 문제

#5.1 9천번이 넘는 리베이스

git rebase main bugFix
git rebase bugFix side
git rebase side another 
git branch -f main another

#5.2 다수의 부모

git branch bugWork main~^2~

#5.3 브랜치 스파게티

git checkout one
git cherry-pick C4 C3 C2
git checkout two
git cherry-pick C5 C4 C3 C2
git branch -f three C2