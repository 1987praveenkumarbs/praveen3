pipeline{
    agent any
    stages{
        stage("test"){
            when{
                changeset "dec1"
            }
            steps{
                sh("uname")
            }
        }
        stage("dev"){
            when{
                changeset "dec1"
            }
            steps{
                echo "Change found in dec1 file"
            }
        }
        stage("prd"){
            when{
                anyOf{
                    changeset "dec1"
                    changeset "dec2"
                }
                
            }
            steps{
                sh("sudo yum install python3-pip* -y")
                sh("sudo pip --version")
                echo "prd stage is success"
            }
            
        }
    }
}
