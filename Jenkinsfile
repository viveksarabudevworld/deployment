pipeline {
    agent any

    stages {
            stage ('Build Stage') {

                steps {
                    withMaven(maven : 'maven_4_0_0') {
                        sh 'mvn clean install'
                    }
                }
            }

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_4_0_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_4_0_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}