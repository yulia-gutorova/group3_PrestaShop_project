pipeline {
    environment {
            PATH = "C:\\WINDOWS\\SYSTEM32;C:\\Program Files\\Java\\jdk-15.0.1\\bin"
    }
    agent {label 'grupp3Jmeter'}
    
    stages{
        stage('Run Jmeter tests') {
            steps {
                bat 'C:\\Tools\\apache-jmeter-5.4.1\\apache-jmeter-5.4.1\\bin\\jmeter.bat -Jjmeter.save.saveservice.output_format=xml -n -t C:\\Tools\\group3_PrestaShop_project\\ThreadGroup.jmx -l jmeter_report.jtl'
                perfReport 'jmeter_report.jtl'
            }
        }
    }
    post {
        success {
            echo 'hello'                     
        }
    }
}