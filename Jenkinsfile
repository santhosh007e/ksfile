node {
    
      stage('git clone') {
      git 'https://github.com/santhosh007e/rh1.git'
    }
       stage('clean') {
       sh 'mvn clean'

    }
	
	   stage('code scan')  {
	{ 
       sh 'mvn sonar:sonar \-Dsonar.host.url=http://35.202.10.40:9000 \-Dsonar.login=3bb4b1e0053e8e1e8a3fef95047c604fd6b97b78'
	}   
       stage('compile') {
       sh 'mvn compile'

    }
       stage('test') {
       sh 'mvn test'

    }
       stage('package') {
       sh 'mvn package'

    }
       stage('deploy') {
       sh 'mvn deploy'    
    }
    }
