pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                bat 'if not exist C:\\deploy mkdir C:\\deploy'
                bat 'copy /Y index.html C:\\deploy\\index.html >nul'

                script {
                    def deployTime = new Date().format(
                        'dd MMMM yyyy, hh:mm:ss a',
                        TimeZone.getTimeZone('Asia/Kolkata')
                    )

                    echo "DEPLOYMENT SUCCESSFUL\nDate : ${deployTime}"
                }
            }
        }
    }
}
