# TwitchBoost
A manager of twitch.tv bots that interact with a channel synchronously but uniquely 

## Credits
TwitchLib - Created by SwitfySpiffy

## Layout
App -> successful input -> insert information to dynamodb -> invoke lambda function

### App
Will host static web app using aws beanstalk or s3 bucket using simple html/css/js
Uppon successful input (payment receieved) will update channelname, #ofbots, time(?)

### Dynamodb
Hold information of past customers as well as in-progress customers

### Lambda
Lambda function will process each new input to the database and instantiate a serverless instance of a bot manager
(not future proof, static IPs? -> Kubernetes(expensive), EC2(overkill + static IP))


#### TODO
Verify twitch account creation scripts work
Create connection to database table that stores information of twitch accounts
Create manager that instantiates bots in a "random" amount of time
Verify inidivual bot functionality
Create front end for web app
Payment processing (bitcoin, ethereum, paypal)

#### COMPLETED
Invidivual bot functionality
