pipeline {
    agent any
    tools {
    	maven 'maven-3.6'
    }
    stages {
    	stage("build jar") {
            steps {
                script {
                    echo "building the application..."
                    sh 'mvn package'
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    echo "building the docker image"
                    withCredentials([usernamePassword(credentialsId: 'nexus-docker-repo', passwordVariable: 'PASS', usernameVariable: 'USER')]) {
                    	sh 'docker build -t dharp3r/java-maven-app:jma-2.0 .'
                    	sh "echo $PASS | docker login -u $USER --password-stdin"
                    	sh 'docker push dharp3r/java-maven-app:jma-2.0'
                    }
                }
            }
        }

        stage("deploy") {
            steps {
                script {
                    echo "deploying the application..."
                }
            }
        }
    }   
}
