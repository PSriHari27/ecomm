pipeline
{
    tools
    {
        jdk 'myjava'
        maven 'mymaven'
    }
    agent none
    stages
    {
        stage('checkout')
        {
            agent any
            steps
            {
                echo 'Cloning the repo'
                git 'https://github.com/PSriHari27/ecomm.git'
            }
        }
        stage('compile')
        {
            agent {label 'Linux_Slave'}
            steps
            {
                
                echo 'compiling the code'
                sh 'mvn compile'
            }
        }
        stage('package')
        {
            agent{label 'Linux_Slave'}
            steps
            {
                sh 'mvn package'
            }
        }
    }
}
