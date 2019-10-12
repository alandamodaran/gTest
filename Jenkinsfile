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
    stage("Checkout repo") {
      steps {
        sh "pwd"
      }

    }
    stage("package") {
      steps {
        sh "echo hello "
      }
    }

    stage("upload to nexus - NOT DEVELOPED") {
      steps {
        sh "echo deploy to  nexus -- to be developed"
      }
    }
    stage("Install in tomcat") {
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

