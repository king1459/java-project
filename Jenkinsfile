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
  }
  }
  
