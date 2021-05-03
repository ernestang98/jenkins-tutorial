pipeline {
    agent{label 'master'}
    tools{maven 'M3'}
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/ernestang98/jenkins-maven-spring.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                sh 'java -jar /Users/ernestang98/.jenkins/workspace/SpringPetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
    
}
