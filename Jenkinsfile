pipeline {
    agent { label 'MASTER'}
    triggers {
        upstream(upstreamProjects: 'dummy', threshold: hudson.model.Result.SUCCESS)
    }
    parameters {
        string(name:'BRANCH_FOR_BUILD', defaultValue: 'master')
    }
    stages {
        stage('Source'){
            steps {
                git url:'https://github.com/sugurumanasa/spring-petclinic.git', branch:"${params.BRANCH_FOR_BUILD}"
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
        }
    }
}
}