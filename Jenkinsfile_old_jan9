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
                    def kout=sh(script:"git diff --name-only HEAD~1 HEAD",returnStdout: true).trim()
                    echo "${kout}"
                    if ("${kout}" == "dec1"){
                        echo "Changes found"
                        error("Changes found it should fail")
                    }
                    else{
                        echo "Changes found in different file"
                    }    
                }    
            }

        }
    }
}
