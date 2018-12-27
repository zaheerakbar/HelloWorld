node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
       // app = docker.build("binuraj/glasslog")
        withDockerServer([uri: 'https://cloud.docker.com/repository/docker']) {
            app = docker.build("binuraj/glasslog")
            // some block
        }
    }

    stage('Test image') {
        app.inside {
            bat 'echo "Tests passed"'
        }
    }

}
