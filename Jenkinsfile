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
                git branch
                git log --oneline
            }

        }
    }
}
