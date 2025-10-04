#1 Push & Pull -- Git 원격 저장소!

##1.1 Clone 소개

git clone

##1.2 원격 브랜치(remote branch)

git commit
git checkout o/main
git commit

##1.3 Git Fetch

git fetch

##1.4 Git pull

git pull

##1.5 가짜 팀워크

git clone
git fakeTeamwork 2
git commit
git pull

##1.6 Git push

git commit
git commit
git push

##1.7 엇갈린 히스토리

git clone
git fakeTeamwork 
git commit
git pull --rebase
git push

##1.8 잠겨버린 main 브랜치

git branch -f main o/main
git checkout -b feature C2
git push origin feature

#2 "origin"그 너머로 -- 고급 Git 원격 저장소

##2.1 Push Main!

git rebase side1 side2
git rebase side2 side3
git rebase side3 main
git pull --rebase
git push

##2.2 원격 작업과 merge하기

git checkout main
git pull
git merge side1
git merge side2
git merge side3
git push

##2.3 원격 저장소 추적하기

git checkout -b side o/main
git commit
git pull --rebase
git push

##2.4 git push의 인자들

git push origin main
git push origin poo

##2.5 git push 인자 -- 확장판!

git push origin main~1:foo
git push origin foo:main

##2.6 Fetch의 인자들

git fetch origin C3:foo
git fetch origin C6:main
git checkout foo
git merge C6

##2.7 Source가 없다

git push origin :foo
git fetch origin :bar

##2.8 pull 인자들

git pull origin C3:foo
git pull origin C2:side

[//] 와! 마지막 레벨까지 마쳤습니다. 멋지네요! (ﾉ^_^)ﾉ (ﾉ^_^)ﾉ (ﾉ^_^)ﾉ