pipeline {
    agent { 
        label 'ROBOSHOP' 
    }
    environment { 
        COURSE= 'Devops'
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'MINUTES') 
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh """
                    echo 'Building.. din-sri'
                    echo "Course name is ${COURSE}"
                    sleep 1
                    echo "Person name is ${params.PERSON}"
                    echo "Biography is ${params.BIOGRAPHY}"
                    echo "Toggle is ${params.TOGGLE}"
                    echo "Choice is ${params.CHOICE}"
                    echo "Password is ${params.PASSWORD}"
                """
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
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
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
    
