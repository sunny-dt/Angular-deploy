node {
    checkout scm

    docker.withRegistry('http://localhost:50000/') {

        def customImage = docker.build("my-image:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}