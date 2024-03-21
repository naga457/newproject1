node {
   stage('Cont.Download') {
   git branch: 'dev', url: 'https://github.com/naga457/newproject1.git'
   }
   stage('Cont.Build') {					  
	sh 'mvn clean package'
			  }
	stage('Cont.Deploy') {		  
	deploy adapters: [tomcat9(credentialsId: '3402421c-3c1b-45d5-ac7d-1e82ab75ec4d', path: '', url: 'http://172.31.14.244:8080')], contextPath: '/dev', war: '**/*.war'	  
			  }		  
     }
