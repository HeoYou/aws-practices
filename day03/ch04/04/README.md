## 예제 실행(AWS에 stack 생성하기)

### ex03
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex03.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```

### ex04
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex04.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```

### ex05
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex05.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```

### ex06
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex06.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```

### ex07
- https://github.com/HeoYou/mysite01/tarball/main
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex07.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```

### ex07
- https://github.com/HeoYou/myapp-basic/tarball/main
```bash
$ aws cloudformation create-stack --stack-name myserver --template-body https://raw.githubusercontent.com/HeoYou/aws-practices/main/day03/ch04/04/ex07.json --parameters ParameterKey=KeyName,ParameterValue=aws-study ParameterKey=VPC,ParameterValue=vpc-00ce686b ParameterKey=InstanceType,ParameterValue=t2.micro

$ aws cloudformation describe-stacks --stack-name myserver --query Stacks[0].Outputs

$ aws cloudformation delete-stack --stack-name myserver
```