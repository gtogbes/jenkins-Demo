pipeline {
	agent {
		label 'Windows_agent'
	}
    	stages {
	    	stage('Checkout-Git') {
        	steps {
                	echo 'Checking out the repository'
                	}
        	}

        	stage('Build') {
        	steps {
                	echo 'running build code'
                	bat 'Build.bat'
                	}
        	}

        	stage('Unit-Test') {
        	steps {
                	echo 'running unit test on code'
                	bat 'Quality.bat'
                	}
        	}

        	stage('Deploy-artefact') {
        	steps {
                	echo 'deploying safe code'
                	bat 'Deploy.bat'
                	}
        	}
			stage('build the java code') {
        	steps {
                	bat 'java hello.java'
                	}
        	}
    	}
}
