pipeline {
    agent any

    stages {
        stage ('Checkout') {
            steps {
                git 'https://github.com/pradipCalsoft/maven-project.git'
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

stage ('Sonar Stage') {

            steps {
                withSonarQubeEnv('sonar') {
                withMaven(maven : 'MyLocalMaven') {
                sh 'mvn clean package sonar:sonar'
                  }
              }
         }        
     } 
  
}
}
