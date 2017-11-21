node ("linux") {
  stage ('Setup'){
    git 'https://github.com/king1459/java-project.git'
    }
  stage ('Unit Tests'){
    sh 'ant -f test.xml -v'
    }
  stage ('Build'){
    sh 'ant -f build.xml -v'
    }
  stage ('Deploy'){
    sh "aws s3 cp /workspace/java-pipeline/dist/rectangle-${env.BUILD_NUMBER}.jar s3://assignment10-s3bucket-paylhna20xyk/"
  }
  stage ('Report'){
   withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'AWS', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
    sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name assignment10'
    }
  }
  }
  
