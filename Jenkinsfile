pipeline {
    agent any
    environment {
        PATH = "D:\apache-maven-3.6.0\bin:$PATH"
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3.6.0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3.6.0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3.6.0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
