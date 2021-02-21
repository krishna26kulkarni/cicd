pipeline{
  agent { label 'agent' }
  
  tools{
    maven 'mvn-3'
  }
  
  stages{
    stage('Pull code'){
      steps{
       checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/krishna26kulkarni/cicd']]])
      }
    }
    stage('Build'){
      steps{
       sh 'mvn clean package'
      }
    }
  }
}
