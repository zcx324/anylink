pipeline {
  agent {
    node {
      label 'jenkins-node1'
    }

  }
  stages {
    stage('error') {
      steps {
        sh '''#!/bin/bash


#IMAGE_NAME="anylink-dev"
IMAGE_VERSION=$(date +\'%Y%m%d\')
REGISTRY_HOST="harbor.atstudy.com"
REGISTRY_NAMESPACE="it-service"
REGISTRY_USERNAME="admin"
REGISTRY_PASSWORD="51testing.bwf"
SSH_HOST="172.16.202.252"
SSH_USER="root"
SSH_PASSWORD="51testing.bwf"


docker build -t $IMAGE_NAME:$IMAGE_VERSION -f docker/Dockerfile .

#docker tag $IMAGE_NAME:$IMAGE_VERSION $REGISTRY_HOST/$REGISTRY_NAMESPACE/$IMAGE_NAME:$IMAGE_VERSION
#docker login $REGISTRY_HOST -u $REGISTRY_USERNAME -p $REGISTRY_PASSWORD
#docker push $REGISTRY_HOST/$REGISTRY_NAMESPACE/$IMAGE_NAME:$IMAGE_VERSION'''
      }
    }

  }
}