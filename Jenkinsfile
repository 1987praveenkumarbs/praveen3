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
                def kout=sh("git diff --name-only HEAD~1 HEAD")
                echo "${kout}"
            }

        }
    }
}
