pipeline{

    agent any
    stages{

        stage('Build'){

            steps{

                sh 'echo "Hello World"'
                sh '''
                echo "MultiLine shell steps work too"
                ls -lah
                '''
            }
        }
    }
}
