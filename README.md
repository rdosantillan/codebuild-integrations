# codebuild-integrations
let's learn codebuild integrations
Codebuild notes
=============


aws cloudformation deploy --template-file codebuild-template.yml \
    --stack-name dev-codebuild-helloworld \
    --parameter-overrides \
    Env=dev \
    BuildSpec=lambda-deploy/sam-upload-buildspec.yml \
    CodeBuildType=lambda-upload \
    Location=https://github.com/rdosantillan/codebuild-integrations \
    SecondaryLocation=https://github.com/rdosantillan/lambdas \
    --tags Env=Dev Course=DevOps \
    --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM