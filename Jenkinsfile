pipeline {
  agent any
  stages {
    stage('DOCKER BUILD & PUSH') {
      steps {
        sh '''echo build in dir: "$(pwd)"

docker build -f ./Dockerfile -t mpcg:20230208 .
docker tag mpcg:20230208 sobev/mpcg:20230208
docker login -u sobev -p dckr_pat_5Zf44zQpMGDrKEA9vkt4ClFKxLo
docker push mpcg:20230208'''
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