pipeline{
  agent any
  stages{
    stage("step1"){
      steps{
        sh("git log --oneline")
      }
    stage("step2"){
      steps{
        sh ("git diff HEAD~1 HEAD")
      }  
    }   
    }
  }
}  
  
  
