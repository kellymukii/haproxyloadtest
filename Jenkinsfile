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
                sh '/home/node/artillery/bin/run run /usr/bin/tanui/haproxy.yml'
            }
        }
    }
}
