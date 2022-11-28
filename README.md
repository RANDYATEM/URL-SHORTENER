#SERVERLESS URL-SHORTENER

Although several Url shortener such as tiny.cc, bit.ly etc already exist, having your own custom URL shortener is always handy when you want to share longer URLs(for example urls gotten from s3 buckets), and with Serverless, building and deploying applications has never been so easy, simple and quick.

* See below image of the architecture designed for this project

<img width="885" alt="Screen Shot 2022-11-27 at 18 19 14" src="https://user-images.githubusercontent.com/100156088/204170418-c255c82d-28d9-4d6e-93ff-d97d44aa54d6.png">

cost considerations

Using a full serverless application has several benefits: the application is natively multi-AZ and automatically scales whether you have one request per month or tens per second.

Now evaluate the cost of the URL shortener for a simple scenario: You create 1000 short URLs per month and each is viewed by 1000 users – i.e., 1 million requests per month. Here is a cost estimate for the Oregon region split by services:

–Lambda: 1000 invocation each of less than 1 second – less than $0.003 / month
–API Gateway: 1000 API calls – less than $0.004 / month
–S3: storage cost is negligible, cost for 1 million GET is $0.04 / month
–Amazon CloudFront: bandwidth cost is negligible, cost for 1 million GET is $0.075 / month
The overall cost is less than 12 cents per month.

The application architecture uses AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Route53, and AWS ACM. 

