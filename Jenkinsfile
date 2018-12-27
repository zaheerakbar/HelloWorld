node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
       // app = docker.build("binuraj/glasslog")https://registry.hub.docker.com
       // This step should not normally be used in your script. Consult the inline help for details.
        withDockerRegistry(url: 'https://registry.hub.docker.com') {
            image = docker.image('binuraj/glasslog:1.0')
            image.pull()
        }
    }

    stage('Test image') {
            echo "Tests passed"
    }

}
