pipeline{
  agent { label 'agent' }
  
  tools{
    maven 'mvn-3'
  }
  
  stages{
    stage('Pull code'){
       checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/krishna26kulkarni/demo']]])
    }
    stage('Build'){
       sh 'mvn clean package'
    }
  }
}
