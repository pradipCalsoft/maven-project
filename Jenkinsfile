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
        sshagent(['8fb2cb27-8756-434d-9d5e-dac83aafce3a']){
                      sh 'scp tlt/target/tlt.war 35.176.184.61:/webapps2'
                      }
            }
      }
        
    }
}
