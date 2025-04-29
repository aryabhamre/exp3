pipeline {
    agent any

    triggers {
        cron('H/2 * * * *')  // Run every 2 minutes
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/aryabhamre/exp3.git'
            }
        }

        stage('Build Java Program') {
            steps {
                sh 'javac addnumbers.java'
            }
        }

        stage('Run Program') {
            steps {
                sh 'java addnumbers'
            }
        }
    }
}
