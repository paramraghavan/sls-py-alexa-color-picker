#Alexa python sdk
https://developer.amazon.com/en-US/docs/alexa/alexa-skills-kit-sdk-for-python/set-up-the-sdk.html

https://github.com/serverless/examples
# https://github.com/serverless/examples/tree/master/aws-python-alexa-skill
# https://www.serverless.com/blog/how-to-manage-your-alexa-skills-with-serverless - original
# https://rupakganguly.com/posts/how-to-build-a-serverless-alexa-skill/
https://github.com/marcy-terui/serverless-alexa-skills *
# Manual hacks:
** https://developer.amazon.com/en-US/docs/alexa/custom-skills/request-and-response-json-reference.html
https://www.serverless.com/framework/docs/providers/aws/events/alexa-skill/
https://medium.com/@rupakg/how-to-build-a-serverless-alexa-skill-51d8479e0432

https://www.serverless.com/blog/building-testing-alexa-skill-bespoken-plugin

https://www.serverless.com/framework/docs/providers/aws/cli-reference/create/

serverless create --template aws-python3
===============================================

# It enables us to manage Alexa skills via the Serverless Framework. 
That is big deal. Without the plugin, you would have to set up the Alexa
skill manually using the Amazon Alexa Skill Developer console.
## sls plugin install -n serverless-alexa-skills

# login to into amazon developer console
https://developer.amazon.com/edw/home.html

Secuitry Profile Name :: ColorPicker
Client id: 
Client Secret : 

Your customer ID: 
Your vendor ID:   

set AMAZON_VENDOR_ID=
set AMAZON_CLIENT_ID=
set AMAZON_CLIENT_SECRET=
set ALEXA_SKILL_ID=
#1 sls alexa auth  
sls alexa auth -h

Run the above command from standalone dos prompt, this auth is valid 
you need to run the above command again to get new token, if and when it expires.


#2 sls alexa create --name LuckyNumber --locale en-US --type custom
==> [Skill ID] amzn1.ask.skill.8e995b14-65b9-4691-965d-1a7a0231944d
above creates a skill 


#3 sls alexa manifests
# +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Serverless:
----------------
[Skill ID] 
[Stage] development
[Skill Manifest]
manifest:
  apis:
    custom: {}
  publishingInformation:
    locales:
      en-US:
        name: ColorPicker
# +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Above lists all your skills you have so far.

update serverless.yml
# sls alexa update

#dummy run
#sls alexa --dryrun
#sls alexa build
#sls alexa models

#sls alexa --dryrun

# sls deploy
Service Information
service: pp-aws-python-alexa-skill
stage: dev
region: us-east-1
stack: pp-aws-python-alexa-skill-dev
resources: 7
api keys:
  None
endpoints:
  None
functions:
  luckyNumber: pp-aws-python-alexa-skill-dev-luckyNumber
layers:
  None

Lambda ARN:
arn:aws:lambda:us-east-1:123456789:function:pp-aws-python-alexa-skill-dev-luckyNumber

update above lambda arn at
apis: custom: endpoint: uri:

sls alexa update
sls alexa build

serverless deploy -v --stage dev
serverless remove -v --stage dev
sls remove
sls alexa delete --id amzn1.ask.skill.7ca0df7a-d59f-4bde-8fb2-c9dac35ae21c


Alexa ask good ducky whats my lucky number
Alexa ask good ducky whats my lucky number lower than 10
Alexa ask good ducky whats my lucky number under 10

# abstract class in python
https://www.geeksforgeeks.org/abstract-classes-in-python/

# online tool to edit text in image file like jpg and save it as an update image file
https://www.photopea.com/learn/


#git not detecting changes to the docx file, just had to reload  from disk
https://stackoverflow.com/questions/16993082/why-doesnt-git-recognize-that-my-file-has-been-changed-therefore-git-add-not-w/24316479

# AWS policy generator
https://awspolicygen.s3.amazonaws.com/policygen.html

# Alexa Slot Type
https://developer.amazon.com/en-US/docs/alexa/custom-skills/slot-type-reference.html

# Alexa Literal Slot type ??
https://developer.amazon.com/blogs/post/Tx3IHSFQSUF3RQP/why-a-custom-slot-is-the-literal-solution
