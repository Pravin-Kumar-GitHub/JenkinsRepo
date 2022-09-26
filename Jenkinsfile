pipeline {
    agent any
    stages {
        stage('test') {
            steps {
                sh 'echo Hello, This is for testing'
            }
        }
        stage('learning') {
            steps {
                git url: 'https://github.com/Pravin-Kumar-GitHub/spring-petclinic.git', 
                    branch: 'main'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('archiving') {
            steps {
                archiveArtifacts '**/*.jar'
            }
        }
    }
}