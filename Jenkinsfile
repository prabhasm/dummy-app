@Library('jenkins-shared-library@feature/start_again') _

pipeline{
  agent any
  stages('build'){
    steps{
      buildTool(
        build: [
          buildType: 'maven'
        ]
      )
    }
  }
}
