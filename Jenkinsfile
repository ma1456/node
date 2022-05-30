pipeline {
  agent { label 'JDK8'}
  options {
      timeout( time:1, unit:'HOURS')
      retry(2)
  }
  triggers{
      cron ( '0 * * * *')
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
    
            
    stage('reporting') {
      steps {
          junit testResults: 'target/surefire-reports/*.xml'
      }
    }
  }
}