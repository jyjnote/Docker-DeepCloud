# Docker-DeepCloud
도커 아키텍쳐
Linux 네이티브
도커는 app을 가상화 VM은 os를 가상화

os=커널(하드웨어와 in,out 하드제어) +유저스페이스(폴더구조+생성)
들어가기전 깃허브에서 좋은거 발견함

컨테이너엔 앱+유저스페이스 포함 관련 파일을 libs에서 찾아 bin에서 app을 실행

윈도우사용자면 짜피 Linux Engine 설치 해야함...

하나의 독립된 컴퓨터라 생각하면 편함
컨테이너 내부로 들어가

```
car /etc/os-release
```
다음 명령어로 해당 컨테이너의 os를 확인 가능. 즉  도커도 os를 가지고 있음 

**도커가 os를 포함안한다 잘못된 지식**


https://github.com/matt9ucci/DockerCompletion에서 
도커 명령어 자동완성 툴 설치하면 편
```
# Install from PowerShell Gallery
Install-Module DockerCompletion -Scope CurrentUser
# Import
Import-Module DockerCompletion
```

docker cloud 사용법

docker images

- 생성
docker run -it 인터레티브 --name 컨테이너 이름 이미지

- 삭제
  docker rmi 이미지
  사용중인 컨테이너가 존재할 경우 삭제 안됨

  docker rm python-conainer 컨테이너 선 삭제

  docker rmi 이미지

  docker stop python-container
  
  docker rm python-container
  
  docker rmi python
  
- search
  ```
  docker search pytoch 이미지 검색
  docker pull pytorch/ptyorch
  docker exec -it python-container /bin/bash 컨테이너로 들어가기
  root@51b37860eb2d:/workspace# python  >>import pytorch
  ```
- 도움말
  docker run --help
  
Azure 결제 및 새팅..

.ssh 이동해서 Azure 머신이름.pem

설치 확인
```
sudo docker run
sudo uesermod -aG docker username

nivida --i
```
nvidia gpu확인
```
docker run --rm --ㅎpus all ubuntu nvidia-smi
```

가상머신 가동
```
cd .sh
ssh -i ~/.ssh/id_rsa.pem(key cont)/ username ip
```

나머진 Azure docs에서 직접 설정...

























