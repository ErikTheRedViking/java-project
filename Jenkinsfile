properties([pipelineTriggers([githubPush()])])

node('linux'){
    stage('Clone'){
        git credentialsId: 'Github', url: 'https://github.com/ErikTheRedViking/java-project.git'
    }
}
