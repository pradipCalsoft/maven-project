pipeline {
    agent any

    stages {
        stage ('Checkout') {

            steps {
                git 'https://github.com/pradipCalsoft/maven-project'
                }
            }
        

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MyLocalMaven') {
                    sh 'mvn test'
                }
            }
        }

stage ('package Stage') {

            steps {
                withMaven(maven : 'MyLocalMaven') {
                    sh 'mvn package'
                }
            }
        }
        
stage ('install Stage') {

            steps {
                withMaven(maven : 'MyLocalMaven') {
                    sh 'mvn install'
                }
            }
        }

    }
}
