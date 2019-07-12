pipeline {
    agent any
    tools {
        maven 'maven'
	}
    stages {
        stage('Initialize') {
	steps {
	    echo 'Validating source code..'
	    sh 'mvn validate'
	    }
	}
	stage('Build') {
	steps {
	    echo 'Building application package..'
	    sh 'mvn clean compile'
            }
        }
        stage('Test') {
	steps {
	    echo 'Starting Unit Test phase..'
	    sh 'mvn test'
	    }
	}
  }
}
