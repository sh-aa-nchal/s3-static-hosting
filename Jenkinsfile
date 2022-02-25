stages{
      stage('deploy to S3'){
          steps{
              sh 'aws s3 cp public/index.html s3://aan-s3-static.test'
              sh 'aws s3api put-object-acl --bucket aan-s3-static.test --key index.html --acl public-read'
              sh 'aws s3 cp public/error.html s3://aan-s3-static.test'
              sh 'aws s3api put-object-acl --bucket aan-s3-static.test --key error.html --acl public-read'
          }
      }
  }
