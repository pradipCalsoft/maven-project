Pipeline{
		agent any{
				Stages{ 
							stage('SCM Checkout'){
							git 'https://github.com/pradipCalsoft/maven-project.git' }
							
							Stage ('Compile Source code'){
							steps{ 
									withMaven (maven: MyLocalMaven)
									sh 'mvn compile'
								  } 
								}
							
							Stage ('Test Source code'){
							steps{
									withMaven (maven:MyLocalMaven)
									sh 'mvn test'
								 }
								}
								
							Stage ('Create Source code package'){
							steps{
									withMaven (maven:MyLocalMaven)
									sh 'mvn package'
								 }
								}	
							Stage ('Install Test'){
							steps{
									withMaven (maven:MyLocalMaven)
									sh 'mvn install'
								 }
								}							
				}				 
		}
	}
