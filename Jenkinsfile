pipeline {
    agent any
	
    tools{
	maven 'apache-maven-3.9.4'
    }
	
    stages {
        stage('Repo-cloning') {
            steps {
                git 'https://github.com/Raghu021/web-project.git'
            }
        }
        stage('maven version'){
            steps {
                sh 'mvn --version'
            }
        }
        stage('mvn-test'){
            steps {
                sh 'mvn test'
            }
        }
        stage('code-pkg'){
            steps {
                sh 'mvn package'
            }
        }
    }
    
}
