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
	agent any
	stages {
		stage('Build') {
			steps {
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
}