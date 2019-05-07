pipeline{
  agent {label 'maven,docker,ansible'}
  stages{
   
              stage('build'){
                steps{
                    withMaven(maven:'localMaven'){
                    sh 'mvn clean package'
                    }
                  }
                }
    stage (‘Deploy’) {
                  sh ‘ssh user@tomcat rm -rf /var/www/temp_deploy/dist/’
    }
        
    }
}
