# welcome

//git명령어
//https://www.youtube.com/watch?v=ZMgLZUYd8Cw&t=514s

git config --global user.name "pnushin"
git config --global user.email "youremail@domain.com"
git clone (url)
git add (file names)
git commit -m "(committed message)
git push -u origin master //(or) git push origin HEAD:master


//docker login

//dockerfile 생성
//https://www.youtube.com/watch?v=ZV2w6b96eEw&t=1836s

//Dockerfile 로 이미지 만들기
nano Dockerfile
{
FROM tomcat:(version)
MAINTAINER (이름)
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install net-tools&&ifconfig
RUN apt-get -y install git
RUN apt-get -y install nano

}

docker build -t tomcat:(tagName) .

//아이피 stop in 관리자cmd
netstat -ano | findstr 3306
taskkill /f /pid (num)

//mysql 실행
docker run --name ARAI_MYSQL -p 3306:3306 -e MYSQL_ROOT_PASSWORD=pwd10404 -d mysql

//우분투 root 접속
su root  
//업데이트
apt-get update
apt-get upgade
//도커설치
apt-get install docker.io
//도커 이미지 풀
docker pull mysql:pnushin
docker pull tomcat:9.0.60-jdk17-temurin-focal
//도커 mysql 실행
docker run --name ARAI_MYSQL -p 3306:3306 -e MYSQL_ROOT_PASSWORD=pwd10404 -d mysql

//실행중인 컨테이너 접속
docker exec -it (CONTAINER ID) /bin/bash
{
apt-get update
apt-get upgrade
//nano설치
apt-get install nano
//ifconfig설치 (ip확인용)
apt-get install net-tools&&ifconfig
//포트확인
netstat -nlpt
//ifconfig로 내부ip확인(172.17.0.3)
ifconfig

//mysql.cnf 찾기 (한글 설정용)
find / -name mysql.cnf
//etc/mysql 에 있음 my.cnf수정
cd /etc/mysql/conf.d/
nano mysql.cnf

//추가하기
{
[client]
default-character-set=utf8

...

[mysql]
default-character-set=utf8

...

[mysqld]
collation-server = utf8_unicode_ci
init-connect='SET NAMES utf8'
character-set-server = utf8
}

//mysql -u root -p pwd10404 bbs < bbsdump.sql
//mysql 접속
mysql -u root -p
{
//db생성 --> 테이블 생성 --> 값 입력
//mysql 나가기
eixt
}
//mysql 컨테이너 나가기
exit

//도커 tomcat 실행 
docker run --name ARAI_tomcat -d -p 80:8080 tomcat:(tagName)
//실행중인 컨테이너 접속
 docker exec -it (CONTAINER ID) /bin/bash
{
//jdk버전 맞추기

wget https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.deb
dpkg -i jdk-17_linux-x64_bin.deb
apt-get install -f
update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-17/bin/java 1
update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-17/bin/javac 1

cd webapps
git clone (url)
cd web1
mv ARAI.war ../
cd..
//기다리기
cd ARAI
}
// 주소 http://localhost/ARAI/main.jsp

$CATALINA_HOME/bin/catalina.sh start
