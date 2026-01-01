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
                sh("git log --oneline")
            }

        }
    }
}
