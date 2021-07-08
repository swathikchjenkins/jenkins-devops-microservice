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
	//agent any
	agent { docker {image 'maven:3.6.3'}}
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
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