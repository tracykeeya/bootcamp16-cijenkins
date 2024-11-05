pipeline {
    agent any
    
    tools {
        maven 'Maven'
    }

    stages {
        stage('compile') {
            steps {
                echo 'Step 1 Compiling our Java App'
                sh 'mvn compile'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Step 2 Run Test'
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                echo 'Step 3 Package'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post {
        always {
            echo "This pipeline is complete"
        }
    }
}
