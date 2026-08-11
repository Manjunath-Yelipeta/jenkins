pipeline {
    agent { 
        label 'ROBOSHOP' 
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                    echo 'Building.. din-sri'
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
                sh '''
                    echo 'Testing.. din-str'
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh '''
                    echo 'Deploying.... din-sri'
                '''
            }
        }
    }
}