# git_memo

## 깃시작
`git init`

작업폴더	

- git add->	staging area
- git commit->	repository(저장소)

### add
```
git add 파일명
git add 파일명 파일명
git add .	//모든파일
```


### commit
`git commit -m "메세지"`

### 상태
`git status`

### 커밋 로그
```
git log --all --oneline
git log --all --oneline --graph	//그래프 보여줌(브랜치보기좋음)
```

### 전 커밋과 차이
```
git diff	//j,k로 스크롤  q는 종료
git difftool
git difftool 커밋아이디	//현재파일vs특정커밋 비교가능 커밋아이디는 로그에 나옴
git difftool 커밋아이디1 커밋아이디2	//커밋아이디1vs커밋아이디2 비교가능 커밋아이디는 로그에 나옴
```

### 브랜치
`git branch 작명`

### 브랜치 위치 변경
`git switch 작명`

### merge
`git merge 작명`

머지 충돌나면 코드 수정후 git add하고 commit

머지 완료된 브랜치 삭제는

`git branch -d 브랜치명`

머지 안한건

`git branch -D 브랜치명`

rebase는 새로운 브랜치에서 git rebase 중심브랜치명 후 중심브랜치에서 git merge


### restore(복구)
```
git restore 파일명
git restore --staged 파일명	//staging 취소
git revert 커밋아이디	//커밋 취소
git reset --hard 커밋아이디 //과거로 다 되돌림
```

### 푸시
```
git branch -M 이름
입력하면 기본 브랜치 이름이 변경

git push -u 원격저장소주소 이름
git remote add 작명 주소
```

### 복사
`git clone 원격저장소주소`

### 기존소스 다른 repository 올릴때
git remote로 설정하고
```
git branch -M main
git push -u origin main
```
