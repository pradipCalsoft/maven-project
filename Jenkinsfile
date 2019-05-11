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
stage('Deploy'){
  steps {
  sshagent (['8d58f2cf-1d45-4f45-87c5-d32f6bdffc45']){
    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.44.203:/var/lib/tomcat/webapps'
  }
}


            }
    
    
        }

    }
}
}
