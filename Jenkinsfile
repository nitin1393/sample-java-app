pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mvn"
    }

    stages {
        stage('Build') {
            steps {
             
                // Run Maven on a Unix agent.
                sh "mvn  clean package"
        }
    }
    stage('Test')
    {
        steps{
            echo "Testing start App"
        }
    }
    stage("Email Notification")
    {
        steps{
             echo  "mail sent"
        }
    }

    stage("Deployment"){
        steps{
            echo "Deployment"
        }
    }
    stage("Install Docke"){
        steps{
            sh 'yum install docker -y'
        }
    }
    stage("Create docker image"){
        steps{
            sh 'docker build -t devops .'
        }
    }
}
}