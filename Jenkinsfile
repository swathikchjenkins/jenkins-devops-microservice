//scripted syntax.
// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"
// 		}
//***
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage ('Integration Test') {
// 		echo "Integration Test"
// 	}
// }

//declarative pipeline syntax.

pipeline {
	//agent { docker { image 'maven:3.6.3' } }
	agent any
	stages {
		stage('Build') {
			steps {
				//sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
			}
	}
		stage('Test') {
			steps {
				echo "Test"
			}
	}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	post {
		always {
			echo "I am good and run always."
		}
		success {
			echo "run when successful"
		}
		failure {
			echo "run when not-successful"
		}
	}
}