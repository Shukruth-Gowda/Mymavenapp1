pipeline{
  agent any
tools{
  maven 'Maven'
}
stages{
        stage('Checkout'){
            steps{
                    git branch:'master',url:''
            }
        }
        stage('Build'){
            steps{
                  sh 'mvn clean install'
            }
        }
        stage('Test'){
            steps{
                  sh 'mvn test'
            }
        }
      stage('Run Application'){
            steps{
                  sh 'java -jar target/Mymavenapp-1.0-SNAPSHOT.jar'
            }
        }
  }
post{
      success{
          echo'Build and depolyment succesfull'
      }
      failure{
          echo'Build failure'
      }
}
            }
            }
