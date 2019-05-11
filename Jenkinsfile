pipeline{
  agent any
  stages{
   
              stage('build'){
                steps{
                    withMaven(maven:'localMaven'){
                    sh 'mvn clean package'
                    }
                  }
                }
    stage ('Deploy') {
      steps{
        sshagent(credentials :['14b465bc-ba00-4474-b831-c0e9d4bf2055']){
                      sh 'scp /var/lib/jenkins/workspace/pipeline1/webapp/target/webapp.war 3.8.124.12'
                      }
            }
      }
        
    }
}
