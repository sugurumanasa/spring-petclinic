pipeline {
    agent { label 'MASTER'}
    triggers {
        upstream(upstreamProjects: 'dummy', threshold: hudson.model.Result.SUCCESS)
    }
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