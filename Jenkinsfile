node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("vijay1229/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.run("-p 49160:8080")
        customImage.push()
    }
}
