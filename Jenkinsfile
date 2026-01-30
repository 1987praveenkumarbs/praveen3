pipeline{
    agent any
    stages{
        stage("test"){
            when{
            changeset "test666.yaml"
            }
            steps{
                sh ("sudo yum install python3-pip* -y")
            }
        }
        stage("dev"){
            when{
                changeset "test666.yaml"
            }
            steps{
                sh ("pip --version")
            }
            
        }
        stage("prd"){
            when{
                changeset "test666.yaml"
            }
            steps{
              sh("sudo pip3 install ansible")   
            }
            
        }
        stage("postprod"){
            when{
                changeset "test666.yaml"
            }
            steps{
                sh("ansible --version")
            }
        }
        stage("final stage"){
            when{
                changeset "test666.yaml"
            }
            steps{
                sh("ansible localhost -m shell -a 'uptime'")
                sh("cp $WORKSPACE/test666.yaml /tmp")
                sh("ansible-playbook  /tmp/test666.yaml")
            }
        }
        
    }
    post{
        always{
            echo "Next step we need to check success or failure"
        }
        failure{
            echo "Any of above stage is failed"
        }
        success{
            echo "Build is sucess"
        }
    }
}
