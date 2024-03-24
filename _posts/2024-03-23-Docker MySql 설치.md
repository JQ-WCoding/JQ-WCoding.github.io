
Docker를 통해 MySQL 설치하는 방법입니다.
  

1. (최신버전) MySQL 설치

```bash
docker pull mysql
```


2. 다운 받은 이미지 확인

```bash
docker images
```

해당 작업을 통해 이미지 다운 여부를 다시 확인합니다.

  

3. 컨테이너 생성 및 실행

```bash
docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password --name sql-name mysql
```

docker run msql를 통해 실행하지만 초기 DB 설정을 위해 추가적으로 port와 passord를 설정합니다.

MYSQL_ROOT_PASSWORD=**password** : 해당 부분에 비밀번호를 설정합니다

--name **sql-name** : 해당 부분에 db 명칭을 설정합니다.

  

4. 확인

```bash
docker ps -a
```

status의 상태가 up 상태여야합니다.

  

5. 컨테이너 접속

```bash
docker exec -it sql-name bash
```

sql-name : 자신이 설정한 db 명칭

  

6. MySQL 서버에 접속하기

```bash
mysql -u root -p
```

이후 password 입력란에 자신이 MYSQL_ROOT_PASSWORD에 설정했던 비빌번호를 작성하면 완료입니다.

  

7. 종료 및 나가기

```bash
exit
```

 구동 중인 서버등을 종료할때 사용하는 command+c 혹은 ctrl+c가 아닌 exit를 사용하여야 합니다.

  

ps. 개인 프로젝트를 위해 docker를 이용한 db를 사용하려 했습니다. 하지만, 무분별하게 사용하기보다 조금 더 검색을 해보니 다른 분들의 글을 통해 보고 배운 바 db 사용을 위해 이용하는 것은 고민해봐야할 문제인 것 같습니다.

  

참고

[https://this-programmer.tistory.com/119](https://this-programmer.tistory.com/119)