node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop todoapp'
            sh 'docker rm todoapp'
            sh 'docker stop todoappdb'
            sh 'docker rm todoappdb'
        }
    }
    stage('Build') {
        build 'BuildDotnetDemoApp'
    }
    stage('Results') {
        build 'TestDotnetDemoApp'
    }
}