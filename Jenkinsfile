pipeline {
	agent any

	stages {
	    stage ('Compile Stage'){
	        steps {
	            withMaven(maven: 'maven'){
	               sh 'mvn compile'
	            }
	        }
	    }

	    stage ('Testing Stage'){
	        steps {
	            withMaven(maven: 'maven'){
	               sh 'mvn test'
	            }
	        }
	    }
	    stage ('Deploy Stage'){
	        steps {
	            withMaven(maven: 'maven'){
	               sh 'mvn clean install'
	            }
	        }
	    }
	}
}
