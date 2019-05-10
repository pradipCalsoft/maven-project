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
        sshagent(['14b465bc-ba00-4474-b831-c0e9d4bf2055']){
                      sh 'scp tlt/target/tlt.war 35.176.184.61:/webapps2'
                      }
            }
      }
        
    }
}
