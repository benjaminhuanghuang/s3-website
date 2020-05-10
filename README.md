# Static website on S3 



## Setup for aws
- Creart IAM user for development
create user and get **Access Key** and the **Secret Access Key**

- Setup aws cli
```
  brew install awscli
  aws configure    # input Access Key and the Secret Access Key
```

- Create S3 bucket
- Create bucket
- Grant public read access to this bucket
- Go to properties, **Static websit hosting**, Select **Use this bucket to host a website** option and index.html
- Set up permission , allow "s3:GetObject"

- Add deply script to package.json
```
  "deploy": "aws s3 sync build/ s3://example-bucket --acl public-read"
```

- The url
http://test>>>.us-east-2.amazonaws.com


