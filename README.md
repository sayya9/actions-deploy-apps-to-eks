# Prerequisites
Create an ECR repo with AWS CLI:
```
aws ecr create-repository --repository-name devops-nginx --region ap-northeast-1
```

Replace the variable `ACCOUNT_ID` with your AWS account ID.

Apply a policy to the repo `devops-nginx`:
```
aws ecr set-repository-policy \
        --repository-name devops-nginx \
        --policy-text file://devops-nginx-ecr-policy.json \
        --region ap-northeast-1
```
![alt text](pictures/actions-deploy-apps-to-eks1.png)
