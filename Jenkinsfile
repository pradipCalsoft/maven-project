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
        sshagent(credentials :['8fb2cb27-8756-434d-9d5e-dac83aafce3a']){
                      sh 'scp webapp-1.0-SNAPSHOT.war.war 35.176.184.61'
                      }
            }
      }
        
    }
}
