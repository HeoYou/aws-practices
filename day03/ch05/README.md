## ch05. 시스템 보안

### 01. 보안 책임
### 02. 소프트웨어 업데이트
### 03. 트래픽 제어
### 04. VPC: 가상 사설 클라우드(네트워크)

### ex07
- https://github.com/HeoYou/myapp-basic/tarball/main
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex03.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```