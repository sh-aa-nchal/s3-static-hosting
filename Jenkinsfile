pipeline {
      agent any
stages{
      stage('deploy to S3'){
          steps{
              sh 'aws s3 cp index.html s3://aan-s3-static.test'
              sh 'aws s3api put-object-acl --bucket aan-s3-static.test --key index.html --acl public-read'
              sh 'aws s3 cp error.html s3://aan-s3-static.test'
              sh 'aws s3api put-object-acl --bucket aan-s3-static.test --key error.html --acl public-read'
          }
      }
  }
post{
        always{
            cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }
}
