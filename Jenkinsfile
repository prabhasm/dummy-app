@Library('jenkins-shared-library@v4.3.4') _

odsComponentPipeline(
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