pipeline {
	agent any
	environment {
	THIS_IS_VAR = 'Iwasset'
	}
	stages{
	 stage('Build time'){
		steps {
		 echo "Im building something, build number ${env.BUILD_ID} on ${env.JENKINS_URL}"
			}
	}
	stage('Validate'){
		steps {
		 echo 'Validate and ${THIS_IS_VAR}' 
		}
	}
	stage('Delivery on Dev'){
	when {
	 branch 'develop' 
	}
		steps{
		echo 'Only on Develop'
		}	
	}
	stage('Delivery'){
	when {
	 branch 'master'
	}
		steps{
	 	 echo 'Only on master'
		}
	}	
   }
}
