Pipeline {
    agent any 

    tools {
        maven 'Maven3'
    }
    stages {
        stage('checkout'){
            steps{
                echo 'downloading src'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building java application'
                sh 'mvn clean compile'
            }
        }

        stage ('Test') {
            steps {
                echo 'Running application tests'
                sh 'mvn test'
            }
        }

        stage ('Package') {
            steps {
                echo 'Creating JAR file'
                sh 'mvn package'
            }
        }
    }
}
