pipeline{

    agent any
    stages{

        stage('Lint HTML'){
        
            sh '''
            tidy -q -e *.html
            
            '''
            
        }
        
        stage('Upload to AWS'){

            steps{

                sh 'echo "Hello World"'
                sh '''
                echo "MultiLine shell steps work too"
                ls -lah
                '''
                
                withAWS(credentials:'aws-static') {
       s3Upload(file:'index.html', bucket:'jenkinsprojectnew', path:'index.html')
}
            }
        }
    }
}
