## 02. 가상 인프라 구축 - ch04. 인프라 프로그래밍 기본

### 01. AWS API 소개

### 02. AWS CLI
    1. 사용자(관리자 권한) 등록
    2. 쉘스크립트 실행 권한 설정 (Windows)
    3-1. 생성 명령
        - aws ec2 describe-images
        -  aws ec2 describe-images --query "Images[?Description=='Amazon Linux 2 AMI 2.0.20210326.0 x86_64 HVM gp2'].ImageId" --output text
        -  aws ec2 describe-vpcs --query "Vpcs[?isDefault==true].VpcId" --output text
        - aws ec2 describe-subnets --query "(Subnets[?VpcId=='vpc-00ce686b'].SubnetId)[0]" --output text
        - aws ec2 create-security-group --group-name mysecuritygroup --description "My Security Group" --vpc-id vpc-00ce686b --output text
        - aws ec2 authorize-security-group-ingress --group-id sg-0904e645ec9509d8c --protocol tcp --port 22 --cidr 0.0.0.0/0
        - aws ec2 run-instances --image-id ami-07464b2b9929898f8 --instance-type t2.micro --security-group-ids sg-0904e645ec9509d8c --subnet-id subnet-1a292d56 --key-name mykey --query "Instances[0].InstanceId" --output text
        - aws ec2 wait instance-running --instance-ids i-00e35e9cd5a4be1c7
    3-2 종료 명령
        -  aws ec2 terminate-instances --instance-ids i-01e4c73fe9f8ac533 --query "TerminatingInstances[0].InstanceId" --output text
        - aws ec2 delete-security-group --group-id sg-0904e645ec9509d8c


### 03. AWS SDK 프로그래밍

### 04. 배포 자동화: Cloud Formation
