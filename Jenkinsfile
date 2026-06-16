pipleline{
	agent any
	
tools{
	maven 'Maven'
}
stages{
	stage('Checkout'){
		steps{
			git branch: 'master',url :'https://github.com/Shukruth-Gowda/Mymavenapp1.git'
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
		sh 'Build and Depolyment successful!'
		}
	failure{
		sh 'Build failure'
		}
	}
	
}
