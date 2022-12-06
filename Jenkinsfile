node {
    
    stage('Gitclone') {
	   
       git branch: 'main', credentialsId: '17b7a009-121f-4c99-992a-7072f18e7018', url: 'https://github.com/rithvikpreethireddy/jenkinsprofinal.git'
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
             -Dsonar.host.url=http://18.140.98.57:9000 \
             -Dsonar.login=bac118450611c8d249690e0255cdc9271fd6e5d4'
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


