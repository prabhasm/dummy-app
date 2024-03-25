@Library('jenkins-shared-library@feature/start_again') _

pipeline{
  agent any
  stage('build'){
    step{
      buildTool(
        build: [
          buildType: 'maven'
        ]
      )
    }
  }
}
