pipeline 
{
    agent any
    triggers
	       {
            pollSCM('* * * * *')
           }
    stages 
    {
        stage('Git Checkout')
        {
            steps
            {
                echo "Accessing pom.xml file from git hub"
                git 'https://github.com/srikanthmvc/java-hello-world-webapp.git'
            }   
        }
        stage('Unit Test')
            {
            steps
            {
                bat 'mvn validate'
        }
    } 
        stage('Commpile' )
        {
        steps
        {
            bat 'mvn compile'
        }
    }    
        stage('Test')
        {
         steps
         {
             bat 'mvn test'
         }
    }
        stage('install')
    {
         steps
         {
             bat 'mvn install'
         }
    }
}
}
