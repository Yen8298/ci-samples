pipeline {
    agent {
        docker {
            image 'katalonstudio/katalon'
            args "-u root"
        }
    }
    
    stages {
        stage('Test') {
            steps {
                sh '"$(pwd)":/Users/yen.nguyen/.jenkins/workspace/Pipleline auto-download katalonc.sh -browserType="Chrome" -projectPath="test.prj" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="c08a2682-fec0-49ad-8691-6d088406b412" -orgID=95893'
            }
        }
    }
}
