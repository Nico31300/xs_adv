@Library('piper-lib-os') _

node() {
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }
    
    stage('xsDeploy') {
	    echo "Deployment on XS Advanced"
	    xsDeploy script: this
    }
}
