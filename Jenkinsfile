pipeline{
  agent any
  environment{
    a="/tmp"
    b="20"
  }
  stages{
    stage("test"){
      steps{
        echo "fetch value is ${a}"
        sh ("uname -r")
        script{
          def kout=sh(script: 'sh /tmp/pp.sh ${a}',returnStdout: true)
          echo "${kout}"
          if("${kout}" =~ "NO issues"){
              echo "Success"
          }
          else{
              echo "Failed"
          }
        }
      }
    }
  } 
}
