#SERVERLESS URL-SHORTENER

Although several Url shortener such as tiny.cc, bit.ly etc already exist, having your own custom URL shortener is always handy when you want to share longer URLs, and with Serverless, building and deploying applications has never been so easy, simple and quick.

* See below image of the architecture designed for this project

<img width="885" alt="Screen Shot 2022-11-27 at 18 19 14" src="https://user-images.githubusercontent.com/100156088/204170418-c255c82d-28d9-4d6e-93ff-d97d44aa54d6.png">

The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon Cognito, and AWS Amplify Console. Amplify Console provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScriot, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway. Amazon Cognito provides user management and authentication functions to secure the backen d API. Finally, DynamboDB provides a persistent layer where data can be stored by API's Lambda function.

Common issues yo could face anf how to resolve it: 
if you are using code commit, makesure you login as Iam user and not rootuser, so as to ba able to configure SSH connections for a root account,since HTTPS connections for a root account are not recommended.
