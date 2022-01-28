pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
               sh "aws cloudformation create-stack --stack-name mywindowsstack --template-body file://vpc-sub-sg-rt-ec2_Windows.yaml"
            }
        }
    }
}