pipeline {
	agent any
  
    environment {
		DOCKERHUB_CREDENTIALS = credentials('DockerHub')
	}
    stages {
        stage('Login') {
		    steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_USR'
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW'
		        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR -p $DOCKERHUB_CREDENTIALS_PSW'
			}
		}
	    stage('git branch') {
		    steps {
			    sh'git branch -a'
		    }
	    }
			    
		    
	    
	
    
//         stage('Build&Push Image') {
//             steps {
//                 sh 'docker build -t 8485012281/jenkins-c2 .'
// 		sh 'docker push 8485012281/jenkins-c2'
//             }
//         }
//         stage('Run Image') {
//             steps {
//                 sh 'docker run -d -p 8020:9191 --name flask_container 8485012281/jenkins'
//             }
//         }
        
//         stage('Test') {
//             steps {
//                 echo 'Successfully Pushed and deploy successfully'
//             }
//         }
         
    }
    }
