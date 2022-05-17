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
		echo "Integration Test"
	}
}


//Declarative Pipeline
pipeline{
	agent any
	// agent { docker {image 'maven:3.6.3'}}
	environment{
		dockerHome = tool 'MyDocker'
		mavenHome = tool 'myMaven'
		PATH  = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "Declarative Pipeline"
				echo "Build stage"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
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
	post{
		always{
			echo 'I always run'
		}
		success{
			echo 'I run when pipeline is successful'
		}
		failure{
			echo 'I run when the pipeline fail'
		}
	}
}