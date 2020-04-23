pipeline{

    agent any
    stages{

        stage('Upload to AWS'){

            steps{

                sh 'echo "Hello World"'
                sh '''
                echo "MultiLine shell steps work too"
                ls -lah
                '''
                
                withAWS(credentials:'aws-static') {
       s3Upload(file:'index.html', bucket:'jenkinsproject3', path:'index.html')
}
            }
        }
    }
}
