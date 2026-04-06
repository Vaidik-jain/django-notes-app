pipeline{
    agent {label "vaidik"}
    stages{
        stage("clone"){
            steps{
                echo "clone"
                git url :"https://github.com/Vaidik-jain/django-notes-app.git",branch :"main"
            }
        }
        stage("build"){
            steps{
                echo "build"
                sh "docker build -t notes-app:latest ."
            }
        }
        stage("test"){
            steps{
                echo "test"
            }
        }
        stage("push to docker hub"){
            steps{
                withCredentials([usernamePassword(
                    credentialsId:"DockerHubCred",
                    passwordVariable :"dockerHubPass",
                    usernameVariable:"dockerHubUser"
                    )]){
                        sh "docker login -u ${env.dockerHubUser} -p ${env.dockerHubPass}"
                        sh "docker image tag notes-app ${env.dockerHubUser}/notes-app"
                        sh "docker push ${env.dockerHubUser}/notes-app:latest"
                    }
            }
        }
        stage("deploy"){
            steps{
                echo "deploy"
                sh "docker-compose up -d"
            }
        }
    }
}
