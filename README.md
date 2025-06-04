회원기능
1. 회원가입을하고 로그인기능이 있으나 익명으로도 가능함
2. 로그인 계정에 한해서 프리미엄계정으로 전환가능(유료)
3. 프리미엄계정에 한해서 기업과 유저들 사이의 후원기능을 통해 수익창출이 가능

게시물기능
1. 게시물 작성시 24시간에서 이슈게시물일 경우 최대 48시간까지 유지가능(사용자가 설정)(이후 자동 삭제)
2. 사진과 동영상이 동반된 게시물이라면 24시간동안 픽셀저하가 차차 생김

메인페이지 ui 기능
1. 기업과 협업해서 기업 광고칸 및 후원홍보창이 상단에 있음 
2. 게시물과 오늘의 기분의 작성란에 따라 컨텐츠 카테고리가 바뀜
3. 이슈 콘텐츠는 상단 추천/홈 분류에서 추천 페이지에 노출 됨.
4. 앱 실행시 index화면에 ai가 물어보는 오늘의 기분은 어떠신가요가 있음
5. 오늘의 기분 전체 통계를 메인 화면 나띵 뉴스 광고 페이지에 슬라이드 형식에 포함.


회원 user  
userID int primary key, auto_increment (고유 아이디)
passWord varchar(20) (비밀번호)
passWord_OK  varchar(20) (비밀번호 확인)
email varchar(30) (이메일)
premium Boolean (프리미엄 여부)

게시물 post
id int primary key, auto_increment (게시물의 고유 번호)
contents  varchar(300) (글 내용)
image_url varchar(200) (이미지 및 동영상)
created_at  datetime (작성 시간)
exprires_at datetime (삭제 예정 시간)

기업 광고 advertising
id int primary key, auto_increment (광고 고유 번호)
image_url varchar(200) (이미지 및 동영상)
