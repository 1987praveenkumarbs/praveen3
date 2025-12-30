pipeline{
  agent any
  stages{
    stage("test"){
      steps{
        sh ("uname;uptime")
        sh ("df -h")
        script{
          def kout=sh(script: "sh /tmp/ml.sh",returnStdout: true)
          echo "${kout}"
          if ("${kout}" -gt 10){
              echo "Issue exsists"
          }
          else{
              echo "Below threshold"
          }
        }
      }
    }
  }
} 
