pipeline {

    agent none

    enviromment {
        DOCKER_IMAGE = "cuongpham082/cupcake"
    }

    stages {
        stage("Build") {
            agent {
                docker {
                    image 'maven:3.9.3-eclipse-temurin-17'
                    args '-v $HOME/.m2:/root/.m2'
                }
            }
            steps {
                 sh 'mvn -B'
            }
        }
    }
}