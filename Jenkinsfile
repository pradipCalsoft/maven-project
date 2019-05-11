pipeline{
agent any
stages{
	stage('SCM checkout'){
		git 'https://github.com/pradipCalsoft/maven-project'
	}
	stage('maven test'){
			steps{
				withMaven(maven: 'MyLocalMaven'){
				sh 'mvn test'
				}
			}
		}
	stage('maven package'){
			steps{
				withMaven(maven: 'MyLocalMaven'){
				sh 'mvn package'
				}
		}
	}
	stage('maven install'){
			steps{
				withMaven(maven: 'MyLocalMaven'){
				sh 'mvn install'
				}
			}
	}
	
	}

}
