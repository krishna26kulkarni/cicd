pipeline{
  agent { label 'agent' }
  
  tools{
    maven 'mvn-3'
  }
  
  stages{
    stage('Pull code'){
      step{
       checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/krishna26kulkarni/cicd']]])
      }
    }
    stage('Build'){
      step{
       sh 'mvn clean package'
      }
    }
  }
}
