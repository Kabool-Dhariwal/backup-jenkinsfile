pipeline{
	agent any
	stages{
		stage('git checkout'){
			steps{
				checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Kabool-Dhariwal/Jenkinsfile.git']])
			}
		}
		stage('compiling'){
			steps{
				bat 'mvn compile'
			}
		}
		stage('packaging'){
			steps{
				bat 'mvn package'
			}
		}
		stage('dependencies'){
			steps{
				bat 'mvn install'
			}
		}
		stage('testing'){
			steps{
				bat 'mvn test'
			}
		}
		
	}
}