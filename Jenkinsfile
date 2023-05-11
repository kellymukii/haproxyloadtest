pipeline {
    agent {
        docker {
            image 'artilleryio/artillery:latest'
            args '-u root:root -i --entrypoint='
        }
    }

 

    stages {
        stage('Load Test') {
            steps {
                sh 'mkdir reports'
                sh '/usr/bin/tanui/haproxy.yml'
            }
        }
    }
}
