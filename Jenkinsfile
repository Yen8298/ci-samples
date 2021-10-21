pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="ed3a88b6-ec9c-4b96-91be-d6ef90e7c53c" -orgID=95893'
                }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'reports/**/*.*', fingerprint: true
            junit 'reports/**/JUnit_Report.xml'
        }
    }
}

