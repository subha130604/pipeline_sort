pipeline {
    agent any
	
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/subha130604/pipeline_sort.git'
            }
        }
        stage('Build') {
            steps {
                dir('D:/maven_Pipe/pipeline') {
                    bat 'mvn clean compile package'
                }
            }
        }
        stage('Test') {
            steps {
                dir('D:/maven_Pipe/pipeline') {
                    bat 'mvn test'
                }
            }
        }
        stage('Run') {
            steps {
                dir('D:/maven_Pipe/pipeline') {
                    bat 'java -cp target/classes com.devops.pipeline.App'
                }
            }
        }
        // Add more stages as needed
    }
}
