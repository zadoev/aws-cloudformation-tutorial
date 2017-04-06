## The basic infrastructure in only five minutes
As a first step, we will set up the basic infrastructure. 


## Infrastructure 
![simple_mockup](../../documentation/images/infrastructure_basic.png)

## Description
The basic infrastructure contains the following AWS resources:

- *Elastic Compute Cloud (EC2)*, two virtual Linux servers called Amazon Linux.
- *Relational Database Service (RDS)* providing a MySQL database.

## Quick Start
1. [Create an IAM User and setup the aws cli](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-set-up.html)
1. Create a key called "keyToSuccess" in the [webinterface](https://console.aws.amazon.com/console/home) -> EC2 -> Key Pairs -> *Create Key Pair*
1. [Download the template](../../templates/stack_basic/template_basic_stack.json)
1. Open a terminal and insert:
```
aws cloudformation create-stack --region us-east-1 --stack-name theStackIsBack --template-body file:///pathToTemplate/template_basic_stack.json --parameters ParameterKey=KeyName,ParameterValue=keyToSuccess ParameterKey=DBName,ParameterValue=TheDbName ParameterKey=DBPwd,ParameterValue=Th3P455w0rd ParameterKey=DBUser,ParameterValue=TheDbUser --capabilities CAPABILITY_IAM
```
<br/><br/>

**Next: [Description of the basic template](../../documentation/basic_stack/template_desc.md)**