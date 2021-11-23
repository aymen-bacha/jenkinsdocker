node{
    def app
    stages{
        stage('clone'){
            checkout scm
        }
        stage('build'){
           app = docker.build('xavki/nginx')
        } 
        stage('test'){
            docker.image('xavki/nginx')withRun('-p 80:80')
            sh 'docker ps'
            sh 'curl localhost'
        }
    }
}