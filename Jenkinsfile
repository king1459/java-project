node {
  agent any
  stage ('Unit Tests'){
    echo 'Unit Tests'
    sh 'ant -f test.xml -v'
    }
  stage ('Build'){
    echo 'Build'
    sh 'ant -f build.xml -v'
    }
  stage ('Deploy'){
  }
  }
  
