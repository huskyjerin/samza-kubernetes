node {
    agent {
        docker { image 'node:9-alpine' }
    } 
   
        stage('Stage 1') {
            steps {

                echo 'Hello world!' 
                sh 'pwd'
            }
        }
        stage('Stage 2') {
            steps {

                echo 'Hello Stage 2!'

               def GRADLE_HOME = tool name: 'gradle', type: 'hudson.plugins.gradle.GradleInstallation'	
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
