# Deploying-Python-website-on-AWS-Elastic-Beanstalk
This Project Simply use of Python framework Django on AWS(Amazon Web Service) Elastic Beanstalk.

Firstly Install Python2.7 and  higher version. 

after installation now install EB Command Line Interface type in command prompt : pip install awsebcli

Now Install virtualenv,type in command prompt : pip install virtualenv

I've Provide two folders in this repository.you can copy into C:\Users\<User Name>> directory.

##Folder 1. aws  

this is use for create virtual environment,so copy this folder anywhere and when you want to activate virtual environment, 

go to top level directory of aws folder after that write command : aws\Scripts\activate

Example : In Windows I've both folder in C:\Users\<User Name>  directory.

then open Command Prompt(without admin) and Enter command :  aws\Scripts\activate

Output will show like :  (aws) C:\Users\<User Name>>

#Folder 2. eb_django_app
this is a django project folder that contains all files whicl will required for create website of python using Django.

 After that write command : pip install django

 Django has been installed , Type : cd eb_django_app

 Now Create an AWS Elastic Beanstalk configuration using the eb init command, 

 specifying the AWS region to use. For example: eb init --region us-west-2
 
 This command launches a command-line wizard that will prompt you with a number of questions to set up your configuration.
 You can accept the default values for most of the questions.
 Here is a short guide to help you fill out your responses:
 
 Select an application to use => accept default: [Create new Application]

Enter Application Name => accept default: eb_django_app

It appears you are using Python. Is this correct? (y/n) => y

Select a platform version. => select your Python version

Do you want to set up SSH for your instances? (y/n) => y

Select a keypair => accept default: Create new keypair

Now Create enviroment name using command ,type : eb create  (the default is your project's directory name)

DNS CNAME prefix(Subdomain Name)  =>  dns_cname_prefix.elasticbeanstalk.com  Here dns_cname_prefix is DNS CNAME,so it define subdomain 

After Successfully finished then Output messgae will show like : INFO: Successfully launched environment: eb-django-app-dev

Now test your application,Type command : eb open

So you will get Successfully Django Python Website running on AWS Elastic Beanstalk.

My Repostory will help directly use files for create Django Python website  and many type of inbuilt commands already executed that save your time.
 see full tutorial at Amazon http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create-deploy-python-django.html#python-django-setup-venv
