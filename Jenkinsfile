@Library("shared") _
pipeline{
    agent {label "vaidik"}
    stages{
        stage("clone"){
            steps{
                echo "clone"
                script{
                clone("https://github.com/LondheShubham153/django-notes-app.git","main")
                }
            }
        }
        stage("build"){
            steps{
                echo "build"
                script{
                    build("notes-app","latest","vaidikjain")
                }
            }
        }
        stage("test"){
            steps{
                echo "test"
            }
        }
        stage("push to docker hub"){
            steps{
               script{
                   push("notes-app","latest","vaidikjain")
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
