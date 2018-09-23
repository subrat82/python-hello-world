pipeline {
  agent none
  stages {
     stage ('checkout') {
	steps {
           git url: 'https://github.com/subrat82/python-hello-world.git/'
	   }
	 }

      stage ('build') {
        steps {
	  sh "'/usr/share/apache-maven/bin/mvn' -X -f  '/var/lib/jenkins/workspace/java-maven-project-from-git/java-maven-app/pom.xml' -Dmaven.test.failure.ignore clean package"
	  }
	}
    }

}
