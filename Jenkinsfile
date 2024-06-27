pipeline {
    agent any 
    
    stages{
        stage("Clone Code"){
            steps {
                echo "Cloning the code"
                git url:"https://github.com/akramul15119/django-notes-app.git", branch: "main"
            }
        }
        stage("Build"){
            steps {
                echo "Building the image"
                sh "docker build -t my-note-app ."
            }
        }
        stage("Deploy"){
            steps {
                echo "Deploying the Server"
                sh "docker-compose down && docker-compose up -d"
                
            }
        }
    }
}


