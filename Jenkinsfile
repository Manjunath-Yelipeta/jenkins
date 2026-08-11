pipeline {
    agent { 
        label 'ROBOSHOP' 
    }
    environment { 
        COURSE= 'Devops'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                    echo 'Building.. din-sri'
                    echo "Course name is ${COURSE}"
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
        post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'I will say Hello only if successful'
        }
        failure { 
            echo 'I will say Bye only if failure'
        }
    }
}
    
