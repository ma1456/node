pipeline {
  agent {

  }
    stages {
        
    stage('Git') {
      steps {
        git url: 'https://github.com/ma1456/node.git',
        branch: 'master'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}