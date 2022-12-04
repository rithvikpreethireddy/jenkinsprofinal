node {
    
    stage('Gitclone') {
	   git branch: 'main', credentialsId: '4c0f65d5-adb2-4590-ac74-a8d82beb347a', url: 'https://github.com/rithvikpreethireddy/jenkinsprofinal.git'
       
    }
	stage('java version') {
	      
           sh 'java -version'
    }
	stage('maven version') {
	       
          sh 'mvn --version'
    }
	stage('maven validate ') {
	       
          sh 'mvn validate'
    }
	stage('sonar scan') {
	      sh 'mvn sonar:sonar \
               -Dsonar.host.url=http://13.212.161.35:9000 \
               -Dsonar.login=e96de5a7e7675eed5c8f96d8a4645803b8ee2c02'
  }
	stage('maven compile') {
	       
          sh 'mvn compile'
    }
	stage('maven test') {
	       
          sh 'mvn test'
    }
	stage('maven package') {
	       
          sh 'mvn package'
    }
        stage('maven deploy') {
		       
          sh 'mvn deploy'
    }
}


