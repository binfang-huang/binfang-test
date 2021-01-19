pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    options {
        timestamps()
    }


    stages {
        stage('First stage') {
            steps {
                echo '-------------------------first stagwe-------------------------'
            }
        }

        stage('Second Stage') {
            steps {
                echo '------------------------second stage-------------------------'
            }
        }

        stage('Third Stage') {
            steps {
                timeout(5) {
                     input 'Continue Third Stage?'
                }
                echo '------------------------third stage-------------------------'
            }
        }
   }
}