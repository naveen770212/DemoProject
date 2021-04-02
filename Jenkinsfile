node {
stage('gitclone') { 
        
        git credentialsId: 'gitaccount', url: 'https://github.com/naveen770212/DemoProject.git'
        
    }
    stage('Build clean') {

      sh 'mvn clean'
         
    }
  stage('sonarqube code scan') {

      sh 'mvn sonar:sonar -Dsonar.host.url=http://34.70.86.196:9000 -Dsonar.login=7997dc722b54cd772f81f0b8ff9465128b52dbc7'
         
    }
	
	stage('Build compile') {

      sh 'mvn compile'
         
    }
  stage('Build test') {

      sh 'mvn test'
         
    }
  stage('Build package') {

      sh 'mvn package'
         
    }
  
  
  stage('Build deploy') {

      sh 'mvn deploy'
    
    
     
    }
}




