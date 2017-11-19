node {
  stage ('Unit Tests'){
    echo 'Unit Tests'
    git 'https://github.com/king1459/java-project.git'
    sh 'ant -f test.xml -v'
    }
  stage ('Build'){
    echo 'Build'
    sh 'ant -f build.xml -v'
    }
  stage ('Deploy'){
    sh 'aws s3 cp /var/jenkins_home/workspaces/java-pipeline/dist/* s3://assignment10-s3bucket-o6pl7q0lmjh9.s3.amazonaws.com'
  }
  stage ('Report'){
    withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AKIAJKQUACHR3WKOHRSA', credentialsId: '059354642686', secretKeyVariable: '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']]){ 
      sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name jenkins'
    }
  }
  }
  
