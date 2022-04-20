@Library('jenkins-library')

def pipeline = new org.js.AppPipeline(
    packageManager:     'npm',
    buildCmds: ["${-> packageManager} run build"],
    steps:              this,
    test:               false,
    dockerImageName:    'iroha2/iroha2-block-explorer-web',
    buildDockerImage:   'docker.soramitsu.co.jp/build-tools/node:14-ubuntu',
    dockerRegistryCred: 'bot-iroha2-rw'
)
pipeline.runPipeline() 