pipeline{
  agent any
  stages{
    stage("test"){
      steps{
        sh ("uname")
        sh ("df -h")
        script{
          def kout=sh(script: 'sh /tmp/ml.sh',returnStdout: true)
          echo "${kout}"
          if ("${kout}" > 10){
              echo "Issue exsists"
              error("Issue exists pipeline shoud fail")
          }
          else{
              echo "Below threshold"
          }
        }
      }
    }
  }
}
