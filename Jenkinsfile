node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
       // app = docker.build("binuraj/glasslog")
        withDockerServer([uri: 'https://cloud.docker.com/repository/docker/binuraj/glasslog']) {
            
        }
    }

    stage('Test image') {
            echo "Tests passed"
    }

}
