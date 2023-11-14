pipeline{
    agent any
    stages{
        stage('cd into test folder'){
            steps{
                sh 'cd $WORKSPACE/comprar-producto-demo'
            }
        }
        stage('execute test'){
            steps{
                sh '/opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo.jmx'
            }
        }
    }
}