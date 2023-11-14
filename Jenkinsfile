pipeline{
    agent any
    stages{
        stage('comprar producto - test'){
            steps{
                sh 'cd $WORKSPACE/comprar-producto-demo && /opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo.jmx'
            }
        }
        stage('generar data - test'){
            steps{
                sh 'cd $WORKSPACE/generar-data-demo && /opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo-GenerarData.jmx'
            }
        }
    }
}