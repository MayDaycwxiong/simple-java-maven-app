pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/MayDaycwxiong/simple-java-maven-app'
                bat 'mvn -B -DskipTests clean package'
            }
        }
    }
}