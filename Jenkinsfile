node {
    
    stage('Gitclone') {
	   git branch: 'main', credentialsId: 'babbly', url: 'https://github.com/rithvikpreethireddy/NAWAZ.git'
       
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
             -Dsonar.host.url=http://18.141.4.150:9000 \
             -Dsonar.login=a8d22f9523f7672f7345d8178c9e88dc247607c7'
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


