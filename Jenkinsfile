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
	    stage ('sonar code smell'){
		    steps {
	   sh 'mvn sonar:sonar -Dsonar.projectKey=project_key -Dsonar.host.url=http://175.41.161.187:9000 -Dsonar.login=4cf8e0c8cc703dfddb541f3a027ec291e8839712'
    }
	    }
    }
	
    
}
