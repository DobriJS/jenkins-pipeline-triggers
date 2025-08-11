pipeline {
    agent any
    // Check for changes in the SCM every minute
   /* triggers {
       pollSCM '* * * * *'
    } */
    
    stages {
        stage('Run Python Script') {
            steps {
                sh 'python3 view_machine_data.py'
            }
        }
    }
    
    post {
        always {
            cleanWs()
        }
    }
}
