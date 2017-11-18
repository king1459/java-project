node {
  stage ('Unit Tests'){
    echo 'Unit Tests'
    echo ls
    sh 'ant -f test.xml -v'
    }
  stage ('Build'){
    echo 'Build'
    sh 'ant -f build.xml -v'
    }
  stage ('Deploy'){
  }
  }
  
