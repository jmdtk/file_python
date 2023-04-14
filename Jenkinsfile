pipeline {
    agent {
        docker {
           image 'dokerfile'
        }
    }
    stages {
        stage('Checkout') {
            steps{
                script{
                    git branch: 'main', url: 'https://github.com/jmdtk/file_python.git'
                    sh "ls -lart ./*"
                }
            }
        }
        stage('exe') {
            steps{
                sh 'python devise.py'
            }
            
        }
    }
    
}
