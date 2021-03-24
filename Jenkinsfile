pipeline {

    agent any

    stages {
        stage('clone') {
            steps {
                // Get some code from a GitHub repository
                sh 'echo "this is the clone stage"'
                sh 'rm -rf Java-hello-world'
                sh 'git clone https://github.com/JavaZakariae/Java-hello-world.git'
            }

        }
        stage('Build') {
            steps {
                sh 'echo "this is the Build stage"'
                sh 'cd Java-hello-world/src/main/java/com/hello && javac Main.java '
            }

        }
        stage('run') {
            steps {
                sh 'java Main'
            }

        }
    }
}
