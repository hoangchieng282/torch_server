pipeline{

	agent {label 'build'}

    stages {
        stage("hehe"){
            steps("test"){
                sh "docker --version"
            }
        }

        stage('Build torchserve image'){
            steps{
                script {
                dockerImage = docker.build("hoangchieng/my-test:${env.BUILD_ID}",".")
                }
                // sh "docker build -t hoangchieng/nodeapp_test:latest ."
                // sh "ls"
            }
        }
    }
        post("Clean up workspace") {
            always {
                cleanWs()
            }
        }



        // stage('Deploy Image') {
        //     agent {
        //         label 'build'
        //     }
        //     steps{
        //         script {
        //             docker.withRegistry( '', "DockerHubCred" ) {
        //                 dockerImage.push()
        //             }
        //         }
        //     }
        // }

}