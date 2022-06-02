
pipeline{
    
    tools{
        jdk "myjava"
        maven "mymaven"
    }
   agent any 
    stages{
        
     stage('clone the repository'){
        steps{
            git 'https://github.com/Sonal0409/DevOpsClassCodes.git'
        }
     }
      stage('compiling'){
        steps{
            sh 'mvn compile'
        }
     }
    
     stage('code review'){
        steps{
            sh 'mvn pmd:pmd'
        }
     }
     stage('unit test'){
        steps{
            sh 'mvn test'
        }
     }
     stage('code coverage'){
        steps{
            sh 'mvn cobertura:cobertura -Dcoberture.report.format=xml'
        }
     }
     stage('package'){
        steps{
            sh 'mvn package'
        }
     }
    }
}
