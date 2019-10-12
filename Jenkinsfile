pipeline {
  parameters {
    string(name: 'REPO', defaultValue:      'https://github.com/alandamodaran/helloWorld.git', description: 'Chart Repository')
    string(name: 'BRANCH', defaultValue:    'master', description: 'Repository Branch')
    string(name: 'APPLICATION', defaultValue: 'helloWorld', description: 'Name of the application to be deployed')
    string(name: 'TOMCATHOME', defaultValue:  '/root/apache-tomcat-9.0.26', description: 'Tomcat path where application to be deployed ')
  }
  agent any

  environment {
    // FOO will be available in entire pipeline
    FOO = "PIPELINE"
  }

  stages {
    stage("STAGE 1 ") {
      steps {
        sh "pwd"
      }

    }
    stage("STAGE 2 ") {
      steps {
        sh date
        sh "echo  hello "
      }
    }

    stage("STAGE 3 ") {
      steps {
        sh "echo STAGE 3 "
      }
    }
    stage("STAGE 4 ") {
      steps {
        sh 'env > env.txt && cat env.txt'

      }
    }
    

  }
  post {
	always {
		cleanWs()
	}
   }
}

