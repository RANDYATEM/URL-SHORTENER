#SERVERLESS URL-SHORTENER

Although several Url shortener such as tiny.cc, bit.ly etc already exist, having your own custom URL shortener is always handy when you want to share longer URLs, and with Serverless, building and deploying applications has never been so easy, simple and quick.

* See below image of the architecture designed for this project
![1_Serverless_Architecture](https://user-images.githubusercontent.com/100156088/203579261-6a250d07-fd35-4942-be05-21e773999808.png)

The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon Cognito, and AWS Amplify Console. Amplify Console provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScriot, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and PI Gateway. Amazon Cognito provides user management and authentication functions to secure the backen d API. Finally, DynamboDB provides a persistent layer where data can be stored by API's Lambda function.

Advantages for using Url shortener:
