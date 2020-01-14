# salesforce-ci-demo #
> This repo contains a demo project developed in Salesforce.com for demonstrating how one can deploy the changes 
> in some org other than in which it is implemented with the help of git, jenkins & Salesforce ANT Migration tool

## Getting Started ##
Developers should have a general understanding that in Salesforce developer org which comes with any trailhead account
doesn't contain facility to create Deployment connections, because there is no facility to create changesets either
inbound or outbound, so Developer need to create a free 30 day trial on Salesforce Dev Hub, using which sandboxes can be 
created and developer can then create deployment connection to test this demo.

Developers should have a general understanding of the following development concepts to better understand the material
presented here :
+ Jenkins (Continuous development build manager)
+ Git (Version control)
+ Salesforce.com
+ ANT (Java framework for automating the deployment of SFDC 'Meta-data' between orgs/sandboxes)

### Steps ###
+ Create Dev Hub account
+ Create 'Dev' and 'QA' org from Dev Hub
+ Create Outbound Connection from 'Dev' org pointing to 'QA' org & create inbound connection in 'QA' org pointing from 'Dev' org
+ Create some custom fields in 'Account' standard object in 'Dev' org which we'll try to deploy into 'QA' org
+ Create change set of this implmentation in 'Dev' org & take export of this change set to your local machine including 'package.xml' with the help of 'build.xml' & 'build.properties'
+ Once export will be completed, few folders will be created in which we have done changes in 'Dev' org
+ Now we're ready for the deployment of this changes into 'QA' org 
+ Login to jenkins server and execute the job so that it can deploy the changes to 'QA' org


