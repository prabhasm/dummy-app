@Library('jenkins-shared-library@feature/start_again') _

pipeline{
  agent any
  stages('build'){
    step{
      buildTool(
        build: [
          buildType: 'maven'
        ]
      )
    }
  }
}
