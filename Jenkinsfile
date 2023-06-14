node {
    echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"

    docker.image('node:lts-slim').inside('-p 3000:3000') {
        stage('Build') {
            sh 'npm install' 
        }
        stage('Test') {
            sh './jenkins/scripts/test.sh' 
        }
    }
}