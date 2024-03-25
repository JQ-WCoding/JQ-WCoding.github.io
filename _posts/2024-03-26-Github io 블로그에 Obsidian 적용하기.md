# Obsidian 설정

해당 설명은 기본 Obsidian 을 세팅하고 사용하신 유경험자를 기반으로 작성하였습니다.
Obsidian의 커뮤니티 플러그인 중 Git을 다운 받아 Github에 자동 백업 연동을 먼저 설정합니다.

1. 커뮤니티 플러그인 Git 다운로드
2. Jekyll 기반 블로그를 사용하면 'posts' 폴더를 중심으로 vault 취급하여 Open Vault하기
   ![[스크린샷 2024-03-25 오후 2.18.34.png]]
3. 커뮤니티 플러그린 자동 Commit/Push/Pull 설정하여 글 작성 시, 자동 업로드하기(5분마다 commit하고, 10분 간격으로 push와 pull 작업을 진행합니다.)
   ![[스크린샷 2024-03-25 오후 2.22.26.png]]

---

# 소스 설정하기

1. 사용자명.github.io 프로젝트 폴더의 '.gitignore' 파일을 수정
2. 'posts' 폴더 하위에 Obsidian 설정 폴더인 .obsidian을 