pipeline{
  agent any
  tools{
    maven 'Maven'
    }
  stages{
    stage('checkout'){
      steps{
      git branch:'master' ,url:'https://github.com/srushtiiik/examaven.git'
      }
     }
    stage('build'){
      steps{
       sh 'mvn clean package'
       }
      }
    stage('deploy'){
      steps{
       sh 'mvn test'
       }
       }
    stage ('run'){
      steps{
        sh 'java -jar target/exmmaven-1.0-SNAPSHOT.jar'
        }
       }
       }
post{
  success{
    echo "succusful"
    }
  failure{
     echo "failure"
     }
     }
}
