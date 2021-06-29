pipeline {
    agent any
    environment {
        PATH="/opt/maven/bin:$PATH"
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Hai') {
            steps {
                echo 'Hai'
            }
        }
        stage('SCM') {
            steps {
              git branch: 'dev', url: 'https://github.com/srinivas1233/maven.git'
            }
        }
         stage('maven') {
            steps {
               sh "mvn clean install"
            }
        }
    }
}
