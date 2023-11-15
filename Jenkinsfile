pipeline{
    agent any
    stages{
        stage('clean workspace'){
            steps{
                cleanWs()
            }
        }
        stage('comprar producto - test'){
            steps{
                sh 'cd $WORKSPACE/comprar-producto-demo && /opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo.jmx'
            }
        }
        stage('generar data - test'){
            steps{
                sh 'cd $WORKSPACE/generar-data-demo && /opt/apache-jmeter-5.6.2/bin/jmeter -n -t Demo-GenerarData.jmx'
                cleanWs()
            }
        }
        stage('upload logs to s3'){
            steps{
                sh 'aws s3 copy $WORKSPACE/generar-data-demo s3://cidemo-npd/$BUILD_NUMBER --recursive  && aws s3 copy $WORKSPACE/comprar-producto-demo s3://cidemo-npd/$BUILD_NUMBER --recursive'
            }
        }
        stage('clean workspace'){
            steps{
                cleanWs()
            }
        }
    }
}