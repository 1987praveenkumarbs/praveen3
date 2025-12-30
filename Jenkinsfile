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
              echo "praveen"
          }
          else{
              echo "Below threshold"
          }
        }
      }
    }
    stage("git operation"){
      when{
        changeset "dec1"
      } 
      steps{
        echo "Changes foud on file dec1"
      }
    }  
        
  }
}
