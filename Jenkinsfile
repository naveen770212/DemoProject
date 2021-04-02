 node {
   
      stage('Git clone') {
        git 'https://github.com/kigrepo/ks.git'
    }
       stage('clean') {
       sh 'mvn clean'
    }
       stage('compile') {
       sh 'mvn compile'
    }
	   stage('sonarqube code scan') {
	   
       sh 'mvn sonar:sonar -Dsonar.host.url=http://34.70.86.196:9000 -Dsonar.login=7997dc722b54cd772f81f0b8ff9465128b52dbc7'
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
