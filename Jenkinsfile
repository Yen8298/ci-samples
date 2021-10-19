pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                dir('/Users/xuan.tran/Downloads/ci-samples-master'){
                sh 'docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest"-apiKey="b7ac7190-fb75-4579-852a-2eb5d69be11d" -orgID=95893'
                }
                }
        }
    }
}
