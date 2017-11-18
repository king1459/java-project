node {
  stage ('Unit Tests'){
    echo 'Unit Tests'
    env.PATH = "${tool 'Ant'}/bin:${env.PATH}"
    sh 'ant -f test.xml -v'
    }
  stage ('Build'){
    echo 'Build'
    sh 'ant -f build.xml -v'
    }
  stage ('Deploy'){
  }
  }
  
