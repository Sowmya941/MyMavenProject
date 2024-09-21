pipeline {
    agent any
    stages {
        stage('Build') {
             steps 
            {
                echo 'Build App'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                // Your test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
                // Your deployment steps here
            }
        }
    }
    post {
        success {
            mail to: 'sowmyasrisunkara519@gmail.com',
                 subject: "Successful Build: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Good news! The build was successful."
        }
        unstable {
            mail to: 'sowmyasrisunkara519@gmail.com',
                 subject: "Unstable Build: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "The build is unstable."
        }
        failure {
            mail to: 'sowmyasrisunkara519@gmail.com',
                 subject: "Failed Build: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Unfortunately, the build failed."
        }
    }
}
