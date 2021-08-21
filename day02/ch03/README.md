## 02. 가상 인프라 구축 - ch03. 가상 서버 EC2

### 01. 가상화와 EC2
1. hyperviso: type1(HVM, PVM), type2
2. AMI(운영체제가 같이 올라간다)
3. Instance

### 02. 가상 서버 시작
1. EC2 인스턴스 생성
2. 가상 서버 시작

### 03. 가상 서버 운영
1. ssh: 가상 서버 접속
    ```bash
    $ ssh -i mykey.pem ec2-user@[public ip]
    ```
2. 가상 서버 모니터링
3. 가상 서버 상태변화
4. 가상 서버 크기

### 04. 네트워크 설정
1. Security Group: 방화벽: 아파치 웹서버 운영
    ```bash
    # yum install -y httpd
    # systemctl enable httpd
    # service httpd [start|stop|restart]
    ```
2. Elastic IP(고정 IP): 아파치 웹 서버 접속
    - 사설 네트워크와 통신 하려면 공용 IP 있어야한다 (검색해서 정리해보자)
    - 라우터 테이블 공부좀 해보자!
3. Network Interface 추가: 2개의 고정 IP로 2개의 웹사이트를 운영
    - 네트워크 카드를 하나 더 달아준다.
    - 그러면 사설아이피가 더 잡힐 것이다.
    - 네트워크 카드가 두개면 퍼블릭아이피를 하나 못잡아준다. 대신에 엘라스틱 아이피 더 받아서 할당한다.
    - 엘라스틱 아이피 두개를 받아서 private ip에 달아준다. 
    - 두개의 네트워크를 사용하는 이유 한개는 RDS를 연결하고 한개는 외부와 연결을 하는거다. 보안을 따로 할 필요가 없다.


