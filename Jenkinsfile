pipeline {
    agent {
        docker { image 'node:9-alpine' }
    } 
    stages {
        stage('Stage 1') {
            steps {

                echo 'Hello world!' 
                sh 'pwd'
            }
        }
        stage('Stage 2') {
            steps {

                echo 'Hello Stage 2!'
                if (isUnix()) {
                 dir('sub-dir'){sh './gradle dockerDistTar'}
                } else {
			dir('sub-dir'){bat 'gradlew.bat clean build'}
		}
                
            }
        }
        stage('Stage 3') {
            steps {

                echo 'Hello world!' 
                sh 'cd /example'
            }
        }
        stage('Stage 4') {
            steps {

                echo 'Hello world!' 
                sh 'pwd'
            }
        }
    }
}
