*개인 로컬에서 작업한 내역을 깃허브 원격 저장소에 커밋하며 협업에 용이한 버전관리 진행<br/><br/>

# Git 초기세팅  
OS 별 CRLF 차이로 인한 문제를 막기 위해 작성  
git config --global core.autocrlf true<br/><br/>

사용자 이름, Email 설정 (되도록 Git에 작성한대로)  
git config --global user.name 'K-Sohyun'  
git config --global user.email 'ksoh912@gmail.com'<br/><br/>

Git Config 설정 확인  
git config --global --list<br/><br/>


# Git 명령어
git init ▶ 새로운 Git 저장소를 생성 (버전관리 시작)<br/>
git add . ▶ 현재 directory 의 모든 파일의 변경사항을 추적<br/>
git commit -m 'Start project' ▶ 메세지(-m)와 함께 버전을 생성<br/>
git status ▶ 파일 상태 확인<br/>
git log  ▶ 커밋 히스토리 조회<br/>
git remote add origin https:// ~ git 주소 ▶ origin이란 별칭으로 원격 저장소를 연결<br/>
git push origin master ▶ origin이란 별칭의 원격 저장소로 master 브랜치의 버전 내역 전송<br/>
git pull origin master ▶ origin이란 별칭의 원격 저장소에서 master 브랜치의 버전 내역 가져옴<br/> 
git branch ▶ 브랜치 목록 조회<br/>
git branch -r ▶ 원격 저장소에 있는 브랜치 목록 조회<br/>
git branch abc ▶ 'abc'란 새로운 브랜치 생성<br/>
git checkout master ▶ 'master' 브랜치로 전환<br/>
git checkout -t origin/xyz ▶ 원격 저장소에 있는 'xyz' 브랜치를 로컬에서 사용<br/>
git checkout -d xyz ▶ 'xyz' 브랜치 삭제<br/>
git clone  https:// ~ git 주소 ▶  해당하는 주소의 저장소를 로컬에 복사<br/>
git reset --hard HEAD~n ▶ 원하는 커밋 버전으로 돌아감 (1은 바로 이전의 버전)<br/>
git reset --hard ORIG_HEAD ▶ 버전 되돌림 취소<br/><br/>


# 브랜치 병합
깃허브 Pull requests 메뉴에서 New pull request 클릭  
병합될 브랜치와 병합할 브랜치 선택 후 Create pull request 클릭  
페이지 전환 후 Pull requests 옆에 추가된 숫자는 현재 오픈된 병합 요청  
Merge pull request 클릭 후 Confirm merge 클릭하면 병합 완료<br/><br/>

# Netlify
깃허브 계정으로 연결 후 사이트 생성 진행 및 확인  
각각의 브랜치에서 작업한 내용은 최종적으로 master 브랜치로 병합, Netlify에선 master 브랜치의 내용만 배포함
