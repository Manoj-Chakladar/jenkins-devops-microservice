//Scripted Pipeline
node {
	echo "Scripted Pipeline:"
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration Test') {
		echo "Test"
	}
}


//Declarative Pipeline
pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				echo "Declarative Pipeline"
				echo "Build stage"
			}
		}
		stage('Test'){
			steps{
				echo "Declarative Pipeline"
				echo "Test stage"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Declarative Pipeline"
				echo "Integration Test stage"
			}
		}
	}
}