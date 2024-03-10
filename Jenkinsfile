@Library('jenkins-shared-library@feature/poc') _

componentPipeline(
  imageStreamTag: 'ods/jenkins-agent-golang:3.x',
  branchToEnvironmentMapping: [
    'master': 'dev',
    // 'release/': 'test'
  ]
) { context ->
  odsComponentStageImportOpenShiftImageOrElse(context) {
    stage('Build') {
      // custom stage
    }
    odsComponentStageScanWithSonar(context)
    odsComponentStageBuildOpenShiftImage(context)
  }
  odsComponentStageRolloutOpenShiftDeployment(context)
}