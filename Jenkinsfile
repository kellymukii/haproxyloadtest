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
                sh '/home/node/artillery/bin/run run /var/lib/jenkins/workspace/artillery-load-test/haproxy2.yml'
            }
        }
    }
}
