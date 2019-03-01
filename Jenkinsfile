pipeline {
	agent any

	stages{
	 stage('Build time'){
		steps {
		 echo 'Im building something'
			}
		}
	stage(Validate){
		steps {
		 echo 'Validate' 
		}
}
	stage(Delivery){
	when {
	 branch 'master'
	}
	steps{
	 echo 'Only on master'
}
}
	}
}
