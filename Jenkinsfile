node {
    checkout scm

    // Run build steps inside a Docker container
    withDockerContainer(image: 'node:16-buster-slim', args: '-p 3001:3000'){
        stage('Build') {
            sh 'npm install' // Install dependencies
        }
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    }
}
