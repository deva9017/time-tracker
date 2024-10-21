pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/deva9017/time-tracker.git'  // Replace with your repository URL
    }

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git branch: 'main', url: "${GIT_REPO}"
            }
        }

        stage('Maven Build') {
            steps {
                // Run Maven build (clean and package the Java project)
                sh './mvn clean package'
            }
        }
    }
}
