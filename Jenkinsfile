pipeline {
    agent any

    stages {
        stage('step 1') {
            steps{

                script{
                    echo "hello"
                    def now = new Date()
                    buildVersion = now.format("yyyy.MM.dd.HHmm", TimeZone.getTimeZone('UTC'))
                    currentBuild.displayName = "${buildVersion}"
                    env.DPLVERSION = "${buildVersion}"
                }
                echo 'Hello world'
            }
        }

        stage('step 2') {
            steps{
                echo "${buildVersion}"
            }
        }

        stage('step 3') {
            steps{
                echo 'End pipeline'
            }
        }
    }
}
