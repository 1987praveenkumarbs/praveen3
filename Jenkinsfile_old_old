pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                echo "praveen"
            }
        }
        stage ("Test") {
            steps {
                sh "/var/git/yu.sh"
                sh ''' #!/bin/bash
                         echo $?
                
                '''                
                
            }
        }
    }
}
