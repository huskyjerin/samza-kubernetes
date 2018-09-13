node {
    agent {
        docker { image 'node:9-alpine' }
    } 
   
        stage('Stage 1') {
           

                echo 'Hello world!' 
                sh 'pwd'
           
        }
        stage('Stage 2') {
           

                echo 'Hello Stage 2!'

               def GRADLE_HOME = tool name: 'gradle', type: 'hudson.plugins.gradle.GradleInstallation'	
		sh "${GRADLE_HOME}/bin/gradle tasks"
		sh "${GRADLE_HOME}/bin/gradle dockerDistTar"               
            
        }
        stage('Stage 3') {
            

                echo 'Hello world!' 
                sh 'cd /example'
            
        }
        stage('Stage 4') {
            

                echo 'Hello world!' 
                sh 'pwd'
            
        }
    
}
