pipeline {
    agent {label 'OPENJDK-11-JDK'}
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('vcs') {
            steps {
                git branch: 'release', url: 'https://github.com/longflewtinku/shopizer.git'         
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}