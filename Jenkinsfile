pipeline{
  agent { label 'agent' }
  
  tools{
    maven 'mvn-3'
  }
  
  stages{
    stage('Pull code'){
      steps{
       git branch: 'main', changelog: false, credentialsId: 'github', poll: false, url: 'https://github.com/krishna26kulkarni/cicd'
      }
    }
    stage('Build'){
      steps{
       sh 'mvn clean package'
      }
    }
  }
}
