pipeline {
  agent any
  stages {
     stage ('checkout') {	
	steps {
           git url: 'https://github.com/subrat82/python-hello-world.git/'
	   }
	 }

      stage ('build') {
	  steps {
       python "'/var/lib/jenkins/workspace/Project1/python-scripts/current-date-time-script.py'"
	  sh "'/usr/share/apache-maven/bin/mvn' -X -f  '/var/lib/jenkins/workspace/java-maven-project-from-git/java-maven-app/pom.xml' -Dmaven.test.failure.ignore clean package"
	  }
	}
    }

}
