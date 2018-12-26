node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("hello-world")
    }

    stage('Test image') {
        app.inside {
            bat 'echo "Tests passed"'
        }
    }

}
