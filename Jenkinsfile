pipeline {
    agent { label 'MASTER'}
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/sugurumanasa/spring-petclinic.git'
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
        }
    }
}
}