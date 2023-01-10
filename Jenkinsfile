#!/usr/bin/env groovy

pipeline{

	agent {label 'build'}

    parameters {
        string(name: 'TRAINNUMBER', description: 'The train number to get artifact')
    }

    stages {
        stage("hehe"){
            steps("test"){
                sh "docker --version"
            }
        }

        stage("test"){
            steps {
                script {
                    sh "ls /var/jenkins_home/workspace/trim_training_demo_mlops_main"
                }
                

            }
        }

        // stage('Build torchserve image'){
        //     steps{
        //         script {
        //         dockerImage = docker.build("hoangchieng/my-test:${env.BUILD_ID}",".")
        //         }
        //         // sh "docker build -t hoangchieng/nodeapp_test:latest ."
        //         // sh "ls"
        //     }
        // }

        
        // stage('Deploy Image') {

        //     steps{
        //         script {
        //             docker.withRegistry( '', "DockerHubCred" ) {
        //                 dockerImage.push()
        //             }
        //         }
        //     }
        // }
    }
        post("Clean up workspace") {
            always {
                cleanWs()
            }
        }





}