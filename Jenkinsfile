pipeline{
  stages{
    node{
              stage('build'){
                steps{
                    withMaven(maven:localMaven){
                    sh 'mvn clean package'
                    }
                  }
                }
        }
    }
}
