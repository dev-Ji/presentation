# presentation
## Docker
도커는 **컨테이너 기반의 오픈소스 가상화 플랫폼**입니다.<br>
<img src = "https://subicura.com/assets/article_images/2017-01-19-docker-guide-for-beginners-1/docker-logo.png" width ="400px" height="400px"><br>
다양한 프로그램, 실행환경을 **컨테이너로 추상화하고 동일한 인터페이스**를 제공하여 프로그램의 배포 및 관리를 단순하게 해줍니다.<br>

컨테이너라 하면 배에 실는 네모난 화물 수송용 박스를 생각할 수 있는데 각각의 컨테이너 안에는<br>
옷,신발,전자제품,술,과일 등 다양한 화물을 넣을 수 있고 규격화되어 컨테이너선이나 트레일러 등 다양한 운송수단으로 쉽게 옮길 수 있습니다.<br><br>
서버에서 이야기하는 컨테이너도 이와 비슷한데 다양한 프로그램,실행환경을 컨테이너로 추상화하고 동일한 인터페이스를 제공하여 프로그램의 배포 및 관리를 단순하게 해줍니다.
데이터베이스 서버, 자바서버 등 어떤 프로그램도 컨테이너로 추상화 할 수 있고 조립PC, AWS, Google cloud등 어디에서든 실행 할 수 있습니다.<br>
<br><hr>
### 컨테이너(Container)란?
컨테이너는 격리된 공간에서 프로세스가 동작하는 기술입니다. 가상화 기술의 하나지만 기존 방식과는 차이가 있습니다.<br>
기존의 가상화 방식은 주로 **OS를 가상화**하였습니다.<br>
<img src = "https://subicura.com/assets/article_images/2017-01-19-docker-guide-for-beginners-1/vm-vs-docker.png" width ="400px" height="400px"><br>
VMware 나 VirtualBox 같은 가상머신은 호스트 OS위에 게스트 OS전체를 가상화하여 사용하는 방식입니다. <br>
이 방식은 여러가지 OS를 가상화(ex:리눅스에서 윈도우를 돌리는것)할 수 있고 비교적 사용법이 간단하지만 무겁고 느려서 운영환경에선 사용할 수 없었습니다.<br>
이를 개선하기 위해 **프로세스를 격리** 하는 방식이 등장합니다.<br>
리눅스에서는 이 방식을 리눅스 컨테이너라고 하고 단순히 프로세스를 격리시키기 때문에 가볍고 빠르게 동작합니다.<br>
CPU 나 메모리는 프로세스가 필요한 만큼만 추가로 사용하고 성능적으로도 거의 손실이 없습니다.<br><br>
하나의 서버에 여러개의 컨테이너를 실행하면 서로 영향을 미치지 않고 독립적으로 실행되어 마치 가벼운 VM을 사용하는 느낌을 줍니다.<br>
실행중인 컨테이너에 접속하여 명령어를 입력할 수 있고 패키지를 설치할 수 있으며 사용자도 추가하고 여러개의 프로세스를 백그라운드로 실행할 수도 있습니다.<br>
새로운 컨테이너를 만드는게 걸리는 시간은 1-2초로 가상머신과 비교도 할 수 없이 빠릅니다.
<hr>

