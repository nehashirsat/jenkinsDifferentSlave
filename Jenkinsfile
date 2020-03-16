pipeline {
    agent none
    stages {

	  stage('demo1') {
	  	    agent {
				kubernetes {
					label 'jenkins-demo1'
					containerTemplate {
						name 'jnlp'
						image 'joao29a/jnlp-slave-alpine-docker:latest'
						resourceLimitCpu '100m'
						resourceLimitMemory '100Mi'
						resourceRequestCpu '100m'
						resourceRequestMemory '100Mi'
					}
				}
			}
            steps {
                build job: 'demo1'
            }
        }
	  stage('demo2') {
	  	    agent {
				kubernetes {
					label 'jenkins-demo2'
					containerTemplate {
						name 'jnlp'
						image 'joao29a/jnlp-slave-alpine-docker:latest'
						resourceLimitCpu '200m'
						resourceLimitMemory '200Mi'
						resourceRequestCpu '200m'
						resourceRequestMemory '200Mi'
					}
				}
			}
            steps {
                build job: 'demo2'
            }
        }
	
    }
}
