node {
    stage('scm') {
        git 'https://github.com/sugurumanasa/spring-petclinic.git'
    }
    stage('build'){
        sh 'mvn package'
    }
}