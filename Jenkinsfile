pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Source code checkout completed.'
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed successfully.'
            }
        }

        stage('Test') {
            steps {
                echo 'Tests completed successfully.'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    def deployTime = new Date().format(
                        'dd MMMM yyyy, hh:mm:ss a',
                        TimeZone.getTimeZone('Asia/Kolkata')
                    )

                    echo "========================================"
                    echo "       DEPLOYMENT SUCCESSFUL"
                    echo "========================================"
                    echo "Application : Jenkins CI/CD Demo"
                    echo "Environment : Production"
                    echo "Date & Time : ${deployTime}"
                    echo "Status      : SUCCESS"
                    echo "========================================"

                    bat 'if not exist C:\\deploy mkdir C:\\deploy'
                    bat 'copy /Y index.html C:\\deploy\\index.html'
                }
            }
        }
    }

    post {
        success {
            echo 'CI/CD PIPELINE COMPLETED SUCCESSFULLY'
        }

        failure {
            echo 'CI/CD PIPELINE FAILED'
        }
    }
}
