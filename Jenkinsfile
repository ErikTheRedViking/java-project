properties([pipelineTriggers([githubPush()])])

node('linux'){
    stage('Clone'){
        git credentialsId: 'Github', url: 'https://github.com/ErikTheRedViking/java-project.git'
    }
    stage('Unit Tests'){
        git credentialsId: 'Github', url: 'https://github.com/ErikTheRedViking/java-project.git'
        sh "ant -f test.xml -v"
        junit 'reports/result.xml'
    }
    stage('Build'){
        git credentialsId: 'Github', url: 'https://github.com/ErikTheRedViking/java-project.git'
        sh "ant -f build.xml -v"
    }
    stage('Deploy'){
        git credentialsId: 'Github', url: 'https://github.com/ErikTheRedViking/java-project.git'
        sh "aws s3 cp /workspace/java-pipeline/dist/rectangle-*.jar s3://hw-10-e/"
    }
}
