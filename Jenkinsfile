@Library('piper-lib-os') _

node() {
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }
    
    /*stage('build') {
        mtaBuild script: this
    }*/

    stage('uploadToTransportRequest') {
        transportRequestUploadFile(
            script: this,
            changeDocumentId: '0000047040',   // typically provided via git commit history
            transportRequestId: 'MFEK900086', // typically provided via git commit history
            filePath: 'WebIDEDemo1.mtar'
        )
    }
}
