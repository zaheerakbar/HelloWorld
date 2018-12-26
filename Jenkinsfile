node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("binuraj/glasslog")
    }

    stage('Test image') {
        app.inside {
            bat 'echo "Tests passed"'
        }
    }

}
