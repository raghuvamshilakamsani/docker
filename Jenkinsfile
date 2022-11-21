  pipeline {
     agent any
     stages {
        stage('git checkout'){
           steps{
                 git clone https://github.com/raghuvamshilakamsani/docker.git
               }
            }
          stage('Build'){
            steps{
                 docker build --tag raghuvamshil/demo:1.0 .
               }
            }
          stage('push'){
             steps{
                  echo "image is pushed to dockerhub"
                  docker push raghuvamshil/demo:1.0
                }
            }
           stage('Deploy'){
              steps{
                   docker run -itd raghuvamshil/demo:1.0
                   echo "docker image is deployed"
                 }
            }
         }
     }
