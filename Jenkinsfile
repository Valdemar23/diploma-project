pipeline {
    agent any 
    stages {
        stage('---applied plugin---') {
            steps {
                sh "mvn -N io.takari:maven:wrapper"
            }
        }
        stage('---package---') { 
            steps {
                sh "mvn package -f diploma-project" 
            }
        }
        stage('deployment project') { 
            steps {
                sh "java -jar ./target/yoda-master-jedi-1.0-SNAPSHOT.jar"  
            }
        }
    }
}
