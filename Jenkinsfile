@Library('jenkins-shared-library@feature/start_again') _

pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        buildTool(
          build: [
            tool_type: 'maven'
          ]
        )
      }
    }
  }
}
