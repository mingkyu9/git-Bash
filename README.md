깃허브에 SSH 원격 접속하기
SSH 원격 접속이란 ? -> 프라이빗 키와 퍼블릭 키를 한 쌍으로 묶어서 컴퓨터를 인증
1. SSH 키 생성하기
$cd ~
$ssh-keygen
엔터 두번 후 프라이빗 키 경로와 퍼블릭 키 경로를 확인
$cd. ssh
$ls -la
프라이빗 키, 퍼블릭 키 확인
2. 깃허브에 퍼블릭 키 전송하기
사용자 컴퓨터의 프라이빗키를 깃허브 서버에 전송한 후 저장 사용자 컴퓨터에서 깃허브 저장속에 접속하면 사용자 컴퓨터에 있는 프라이빗 키와 깃허브 서버에 있는 퍼블릭 키를 뵤하여 저장소가 연결
$ clip <~/.ssh/id_rsa.pub
3. SSH 주소로 원격 저장소 연결하기
$ cd ~
$ git init connect-ssh
$ cd connect-ssh
$ git remote add origin 복사한 주소 붙여넣기
$ gir remote -v
$ git push -u origin main

