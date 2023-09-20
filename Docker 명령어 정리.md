
**docker images (이미지 확인)**
```
$ docker images
```

**docker pull (이미지 다운)**
```
$ docker pull centos
```

**docker create (이미지로 컨테이너 생성)**
```
## -i 는 상호 입출력
## -t 는 tty를 활성화해서 bash 셸을 사용
$ docker create -i -t centos

## 만약 이름을 설정하고 싶다면 "--name" 옵션을 추가하여 "컨테이너 이름"을 설정할 수 있다.
$ docker create -i -t --name (내가 설정하려는 컨테이너 이름) (이미지 이름)
$ docker create -i -t --name mycontainer centos
```

**docker start (생성된 컨테이너 실행)**
```
## docker create로 컨테이너를 생성했다면 시작후 사용 가능하다.
$ docker start mycontainer
```

**docker attach (컨테이너 접속)**
```
## 컨테이너가 Up 상태일 경우 attach 명령어를 사용해서 접속이 가능하다.
$ docker attach mycontainer
```

**docker run (이미지로 컨테이너 생성 및 실행)**
```
- docker create + docker start + docker attach를 한번에 실행하는 것과 같음
- 이미지가 없을 경우 도커 허브에서 최신이미지를 자동으로 pull
```


**docker exec (컨테이에 특정 명령을 실행)**
```
docker exec <CONTAINER_ID> <COMMAND>

추가)
run & exec & attach 차이
```

*ref.* https://0902.tistory.com/4