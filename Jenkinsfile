pipeline{
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'g++ PES1UG20CS411_test.cpp'
        build job : 'PES1UG20CS411-1'
        echo 'Build successful'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
        echo 'Test successful'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deploy successful'
      }
    }
  }
  post{
    failure{
      echo 'Failed'
    }
  }
}
