Pipeline{
  tools{
    maven 'Maven'
    }
  stages{
    stage('checkout'){
      step{
      git branch:'master' ,url:'https://github.com/srushtiiik/examaven.git'
      }
     }
    stage('build'){
      step{
       sh 'mvn clean package'
       }
      }
    stage('deploy'){
      step{
       sh 'mvn test'
       }
       }
    stage ('run'){
      step{
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
