pipeline{
agent any
stages{
	stage('SCM checkout'){
		git 'giturl'
	}
	stage('maven test'){
			steps{
				withMaven(maven: 'localMaven'){
				sh 'mvn test'
				}
			}
		}
	stage('maven package'){
			steps{
				withMaven(maven: 'localMaven'){
				sh 'mvn package'
				}
		}
	}
	stage('maven install'){
			steps{
				withMaven(maven: 'localMaven'){
				sh 'mvn install'
				}
			}
	}
	
	}

}
