pipeline {
  agent any
  stages {
    stage('DOCKER BUILD & PUSH') {
      steps {
        sh '''sudo su
echo build in dir: "$(pwd)"

sudo docker build -f ./Dockerfile -t mpcg:20230208 .
sudo docker tag mpcg:20230208 sobev/mpcg:20230208
sudo docker login -u sobev -p dckr_pat_5Zf44zQpMGDrKEA9vkt4ClFKxLo
sudo docker push mpcg:20230208'''
      }
    }

    stage('PULL IMAGE & RESTART') {
      steps {
        sh '''echo "pulling image"

echo "restarting server"

echo "restarting success"'''
      }
    }

  }
}