pipeline{
    agent any
    stages{
        stage('cd into folder'){
            steps{
                sh 'cd comprar-producto-demo'
            }
        }
        stage('execute test'){
            steps{
                sh '/opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo.jmx'
            }
        }
    }
}