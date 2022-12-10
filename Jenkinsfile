pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                timeout(time: 5, unit: 'MINUTES') {
                    retry(2) {
                        sh 'kubectl create -f https://raw.githubusercontent.com/raman-engr/myGit/master/deploy-2.yaml'
                    }
                }
            }
        }
    }
}