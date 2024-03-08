pipeline{
    agent any
    stages{
        stage('build'){
            steps {
                build '_PES1UG21CS038-1'
                sh 'g++ main.cpp -o output'
            }

        }
        stage('test'){
            steps{
                sh './output'
            }
        }
        stage('deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
            failure{
                error 'pipeline failed'
            }
    }
}
