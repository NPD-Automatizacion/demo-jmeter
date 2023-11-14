pipeline{
    agent any
    stages{
        stage('execute test'){
            steps{
                sh 'cd $WORKSPACE/comprar-producto-demo && /opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo.jmx'
            }
        }
    }
}