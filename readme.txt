good article:  https://dashbird.io/blog/lambda-kinesis-trigger/
cloned repo:   https://github.com/vingao/aws-kinesis-trigger

yarn install
yarn run deploy --region us-east-1
yarn run remove --region us-east-1
yarn run produce --region us-east-1  (outside fmn)

cloudwatch log insights for /aws/lambda/betterdev-dev-kinesisPitfalls-consumer with query:
fields data.count
| filter message = 'Records count'
| sort @timestamp desc