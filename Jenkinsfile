pipeline {
    agent any

    tools {
        nodejs 'node25' 
    }

    stages {
        stage('Checkout') {
            steps {
                // यह आपके GitHub से कोड उठाएगा
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing packages...'
                // विंडोज के लिए 'bat', लिनक्स के लिए 'sh' का प्रयोग करें
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Building React App...'
                bat 'npm run build'
            }
        }

        stage('Display Status') {
            steps {
                echo 'Build Successful!'
            }
        }
    }
}