#!/usr/bin/groovy

@Library('github.com/piyush1594/fabric8-pipeline-library@nodejs')
def canaryVersion = "1.0.${env.BUILD_NUMBER}"
def utils = new io.fabric8.Utils()
def stashName = "buildpod.${env.JOB_NAME}.${env.BUILD_NUMBER}".replace('-', '_').replace('/', '_')
def envStage = utils.environmentNamespace('stage')
def envProd = utils.environmentNamespace('run')
def setupScript = null


  nodejsNode { 
      container(name: 'nodejs') {
          echo "Nodejs Image"
          sh "echo Nodejs"
          sh "npm version"
          sh "node --version"
      }
  }
