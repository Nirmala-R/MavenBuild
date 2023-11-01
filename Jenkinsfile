pipeline {
  agent any
	stages {
	stage ('Build'){
		steps {
		sh "mvn clean install -Dmaven.test.skip=true"
		}
	}

	//stage ('Test Cases Execution'){
		//sh "mvn clean org.jacoco:jacoco-maven-plugin:prepare-agent install -Pcoverage-per-test"
	//}

	//stage ('Sonar Analysis'){
		//sh 'mvn sonar:sonar -Dsonar.host.url=http://52.90.114.217:9000 -Dsonar.login=3f2d512066c968a048575e6a0001e6bcffe61601'
	//}

	//stage ('Archive Artifacts'){
		//archiveArtifacts artifacts: 'target/*.war'
	//}
	
	stage ('Deployment'){
		steps{
		sh 'cp /var/lib/jenkins/workspace/tomcatserverjob/target/*.war /usr/local/tomcat9/webapps'
	}
	}
	//stage ('Notification'){
		//slackSend color: 'good', message: 'Deployment Sucessful'
		//emailext (
		      //subject: "Job Completed",
		      //body: "Jenkins Pipeline Job for Maven Build got completed !!!",
		      //to: "nimi.saravanan@gmail.com"
		    //)
	//}
}
}

	
