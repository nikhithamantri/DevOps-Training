timestamps {
    node('Windows') {
        stage('checkout'){
            git credentialsId: 'Git', url: 'https://github.com/nikhithamantri/DevOps-Training.git'
        }
        stage('Hello') {
            bat label: '', script: 'echo "[INFO] This is running on Windows"'
        }
    }
        
    node('master') {    
        stage('calling shell'){
                sh label: '', script: '''#!/bin/bash
                    echo "[INFO] Directly excuting it from Jenkins"
                    echo "[INFO] Directly excuting it from Jenkins" > New.txt
                    echo ${param1} >> jenkins.txt
                    echo ${WORKSPACE} >> jenkins.txt
                    echo ${choice} >> jenkins.txt
                    echo ${GIT_BRANCH}'''            
        }
        
        stage('echo') {
                echo 'This is Second Stage!'
        }
    }
}
