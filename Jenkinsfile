pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAws(region: 'us-east-1', credentials:'aws-static'){
                        sh 'echo "Uploading content with AWS credentials"'
                            s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html',  bucket:'jenkins-udacity-project-static-crisr')

                    }
                }
            }
        }
}