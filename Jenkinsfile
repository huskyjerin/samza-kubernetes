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

               sh 'wget https://services.gradle.org/distributions/gradle-3.4.1-bin.zip'
		sh 'sudo mkdir /opt/gradle'
		sh 'sudo unzip -d '/opt/gradle gradle-3.4.1-bin.zip'
		sh 'export PATH=$PATH:/opt/gradle/gradle-3.4.1/bin'
		sh 'gradle -v'
		sh 'gradle dockerDistTar'               
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
