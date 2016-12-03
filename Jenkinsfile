def loadUtils() {
    def utils

    fileLoader.withGit('https://github.com/nicktate/containership.cloud.jenkins-pipeline.git', 'master', 'containershipbot_github_user_pass', '') {
        utils = fileLoader.load('Jenkinsfile')
    }

    return utils
}

def utils
node {
    stage('Preparation') {
        utils = loadUtils()
        echo "Loaded Containership Jenkins Utils"
    }
}

utils.runPipeline()
