pipeline {
    agent any
    
    options { timestamps () }
    
    environment {
        GOROOT = '/usr/local/go'
        PATH = '/usr/local/bin:/usr/bin:/bin:/usr/local/go/bin'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    currentBuild.description = "Building on ${env.NODE_NAME}"
                }
                sh 'go run hello-world.g'
            }
        }
    }
}
