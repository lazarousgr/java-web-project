pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('Deploy') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '9f5d34e9-db4b-4da8-89a7-01fef94593fa',path: '',
                url: 'http://192.168.1.28:9999/')], contextPath: 'javawebapp',
                war: '**/java-web-project.war'
                
            }
        }
    }
}
