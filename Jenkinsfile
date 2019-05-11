Pipeline{
		any agent{
				Stages{ 
							stage('SCM Checkout'){
							git 'Github URL' }
							
							Stage ('Compile Source code'){
							steps{ 
									withmaven (maven: MyLocalMaven)
									sh 'mvn compile'
								  } 
								}
							
							Stage ('Test Source code'){
							steps{
									withmaven (maven:MyLocalMaven)
									sh 'mvn test'
								 }
								}
								
							Stage ('Create Source code package'){
							steps{
									withmaven (maven:MyLocalMaven)
									sh 'mvn package'
								 }
								}	
							Stage ('Install Test'){
							steps{
									withmaven (maven:MyLocalMaven)
									sh 'mvn install'
								 }
								}							
				}				 
		}
	}
