pipeline {
    agent any
    tools {
        maven 'Maven'
        jdk 'jdk'
    }
    stages {
        stage ('Clone') {
            steps {
                git branch: 'master', url: "https://github.com/Nouman72884/maven-s3-repo.git"
            }
        }
        stage ('build stage') {
            steps {
                //sh 'mvn clean install package'
                sh 'mvn  clean install'
            }
        }
        // stage ('publish artifacts') {
        //     steps {
        //         sh 'cd ../..'
        //         sh 'ls'
        //         s3Upload consoleLogLevel: 'INFO', dontSetBuildResultOnFailure: false, dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'nouman-work', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: true, noUploadOnFailure: true, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: '~/. m2/repository/', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'artifacts', userMetadata: []
        //     }
        // }
        // stage ('upload artifacts') {
        //     steps {
        //         script {
        //             withAWS(region: 'us-east-1',credentials:'aws-credentials-nouman') {
        //                 s3Upload(file:'/var/lib/jenkins/.m2/repository/', bucket:'nouman-work', path:'artifacts/')    
        //                     }
        //         }
        //     }
        // }
    }
}