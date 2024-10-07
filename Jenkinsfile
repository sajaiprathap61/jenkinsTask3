pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }

    post {
        success {
            mail to: 'sajaiprathap61@gmail.com',
                 subject: "Successful Build: ${currentBuild.fullDisplayName}",
                 body: "Good news! The build was successful. Check it out here: ${env.BUILD_URL}"
        }
        failure {
            mail to: 'sajaiprathap61@gmail.com',
                 subject: "Failed Build: ${currentBuild.fullDisplayName}",
                 body: "Oh no! The build has failed. Check the logs here: ${env.BUILD_URL}"
        }
    }
}

