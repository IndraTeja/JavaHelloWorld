pipeline { 
    agent any
    stages { 
        stage('source') {
            steps {
                echo 'SCM....'
                git 'https://github.com/IndraTeja/JavaHelloWorld.git'

            }

        }
        stage('build') {
            steps {
                echo 'Building....'
                sh ''' 
                java -version
                javac HelloWorld.java
                java HelloWorld
                
                '''
            }
        }
        stage('test') {
            steps {
                echo 'Calling Second Function...'
                sh ''' 
                
                curl -I -u user2:118949419cf2b1b581d2f5f1c8b28fefbd http://10.1.2.109:8080/job/SecondJob/build?token=kIUfDV6uKmLAbHaByGbSvuxDddNkWABu
                
                '''
            }
            
        }
        
    }
}
