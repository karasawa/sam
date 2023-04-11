# sam

sam用のテンプレート置き場

aws s3 mb s3://sam-demo

sam package --template-file template.yaml --s3-bucket sam-demo --output-template-file packaged.yaml

sam deploy --template-file packaged.yaml --stack-name sam-demo --capabilities CAPABILITY_IAM

aws s3 rm s3://sam-demo --recursive