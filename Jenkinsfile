pipeline {
	agent any
		stages {
			stage('Build') {
				steps {
					echo 'Hello world!'
					echo 'Coucou !'
					echo 'Welcome !'
					script {
						docker.withTool('latest') {
						docker.image('maven:3-jdk-8-slim').inside("-v $WORKSPACE:/usr/src/HelloWorld:rw -v
						$HOME/.m2:/root/.m2:rw -w /usr/src/HelloWorld") { c ->
						sh "mvn clean package"
						}
					}
				}
			}
		}
	}
}
