pipeline {
	agent any
	environment {
	THIS_IS_VAR = 'Iwasset'
	}
	parameters {
        string(name: 'THIS_IS_PARAM', defaultValue: 'DEV ENV', description: 'Set by params')
    }
	stages{
	 stage('Build time'){
		steps {
		 echo "Im building something, build number ${env.BUILD_ID} on ${env.JENKINS_URL}"
			}
	}
	stage('Validate'){
		steps {
		 echo "Validate and ${env.THIS_IS_VAR}"
		}
	}
	stage('Delivery on Dev'){
	when {
	 branch 'develop' 
	}
		steps{
		echo "Only on Develop and received ${params.THIS_IS_PARAM}"
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
