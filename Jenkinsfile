<<<<<<< HEAD
<<<<<<< HEAD
@Library('jenkins-shared-library')
def gv

=======
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
=======
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
pipeline {
    agent none
    stages {
    	stage("test") {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Executing pipeline for branch $BRANCH_NAME"
                }
            }
        }
<<<<<<< HEAD
<<<<<<< HEAD
        stage("build jar") {
            steps {
                script {
                    echo "building jar"
                    buildJar()
=======
=======
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == 'master'   
<<<<<<< HEAD
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
=======
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
                }
            }
            steps {
                script {
<<<<<<< HEAD
<<<<<<< HEAD
                    echo "building image"
                     buildImage()
=======
                    echo "Building the application..."
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
=======
                    echo "Building the application..."
>>>>>>> d6daee232b6de0ea9324e7a03f67771d53cf3ff8
                }
            }
        }

        stage("deploy") {
            when {
                expression {
                    BRANCH_NAME == 'master'   
                }
            }
            steps {
                script {
                    echo "deploying the application..."
                }
            }
        }
    }   
}
