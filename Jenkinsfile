pipeline {
    agent any

    environment {
        FIREBASE_TOKEN = credentials('FIREBASE_TOKEN')
    }

    stages {
        stage('Install Firebase CLI') {
            steps {
                bat 'npm install -g firebase-tools'
            }
        }

        stage('Deploy to Firebase') {
            steps {
                bat "firebase deploy --token %FIREBASE_TOKEN%"
            }
        }
    }
}