# 環境構築

## CDK CLIのインストール

```
npm install -g aws-cdk
```

## bootstrapの実行

> Many AWS CDK stacks that you write will include assets: external files that are deployed with the stack, such as AWS Lambda functions or Docker images. The AWS CDK uploads these to an Amazon S3 bucket or other container so they are available to AWS CloudFormation during deployment. Deployment requires that these containers already exist in the account and region you are deploying into. Creating them is called bootstrapping.

https://docs.aws.amazon.com/cdk/v2/guide/getting_started.html

```
cdk bootstrap aws://<アカウントID>/<リージョン名>
```

## ディレクトリの作成

```
mkdir hello-cdk
cd hello-cdk
```

## アプリケーションの作成

> Each AWS CDK app should be in its own directory, with its own local module dependencies. Create a new directory for your app. Starting in your home directory, or another directory if you prefer, issue the following commands.

https://docs.aws.amazon.com/cdk/v2/guide/hello_world.html

```
cdk init app --language typescript
```

# CDKのコマンド

- cdk list (ls)
    - Lists the stacks in the app
- cdk synthesize (synth)
    - Synthesizes and prints the CloudFormation template for the specified stack(s)
- cdk deploy
    - Deploys the specified stack(s)
- cdk destroy
    - Destroys the specified stack(s)
- cdk diff
    - Compares the specified stack with the deployed stack or a local CloudFormation template

https://docs.aws.amazon.com/cdk/v2/guide/cli.html
