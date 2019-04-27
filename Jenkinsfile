properties([pipelineTriggers([githubPush()])])

node('linux'){
    stage('Clone'){
        git credentialsId: 'Github_access_token_for_Jenkins', url: 'https://github.com/ErikTheRedViking/java-project.git'
    }
}
