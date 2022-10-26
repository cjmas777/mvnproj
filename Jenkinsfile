pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/cjmas777/mvnproj.git'

            }
        }
        stage('Build') {
            steps {
                // build maven project
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

            }
        }
        stage('publish on tomcat server') {
            steps {
                // build maven project
                sh 'cp **/* /var/lib/tomcat9/webapps/'
                
            }
        }
    
    }
}
