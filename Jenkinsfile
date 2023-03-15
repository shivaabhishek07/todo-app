pipeline{
    agent any
    stages{
        stage('Git'){
            steps{
                git branch: 'main', url: 'https://github.com/shivaabhishek07/todo-app'
            }
        }
        stage ('Build'){
            steps{
                sh 'sudo docker build -t nodejs-todo .'
            }
        }
        stage ('Run'){
            steps{
                sh 'sudo docker run -d -p 8000:8000 nodejs-todo'
            }
        }
    }
}
