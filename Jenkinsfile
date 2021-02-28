pipeline {
	agent any
	stages {
		stage("Compile"){
			steps {
				bat "mvn compiler:compile"
			}
		}
		stage("Test"){
			steps {
				bat "mvn surefire:test -Dtest=MavenJenkinsTest" 
			}
		}
		stage("Package"){
			steps {
				bat "mvn jar:jar"
			}
		}
		stage("Deploy"){
			steps {
				bat "mvn install:install-file -Dfile=target/jenkinsfile-1.jar"
			}
		}
	}
}
