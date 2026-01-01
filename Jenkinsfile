pipeline{
    agent any
    stages{
        stage("test1"){
            steps{
                sh("uname")
            }
        }
        stage("test2"){
            steps{
                sh("git branch")
                sh("git diff --name-only HEAD~1 HEAD")
                script{
                    def kout=sh(script:"git diff --name-only HEAD~1 HEAD",returnStdout: true)
                    echo "${kout}"
                }    
            }

        }
    }
}
