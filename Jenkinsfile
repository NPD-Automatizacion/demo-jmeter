pipeline{
    agent any
    stages{
        // stage('installing jmeter plugins'){
        //     steps{
        //         sh 'cd /opt/apache-jmeter-5.6.2/lib && java -jar cmdrunner-2.3.jar --tool org.jmeterplugins.repository.PluginManagerCMD install-for-jmx $WORKSPACE/comprar-producto-demo/Demo.jmx'
        //     }
        // }
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