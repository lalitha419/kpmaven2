@Library('libraries')_
pipeline
{
    agent any
    stages
    {
        stage('continuos download')
        {
            steps
            {
                script
                {
                    cicd.newgit("https://github.com/lalitha419/kpmaven2.git")
                }
            }
        }
        stage('continuos build')
        {
            steps
            {
                script
                {
                    cicd.newmaven()
                }
            }
        } 
        stage('continuos deploy')
        {
            steps
            {
                script
                {
                    cicd.newdeploy("172.31.9.80","testapp")
                }
            }
        }   
        stage('continuos testing')
        {
            steps
            {
                script
                {
                    cicd.newgit("https://github.com/intelliqittrainings/FunctionalTesting.git")
                    cicd.runselinium("/home/ubuntu/.jenkins/workspace/declarativepipeline1")
                }
            }
        } 
        stage('continuos delivery')
        {
            steps
            {
                script
                {
                    cicd.newdeploy("172.31.14.99","prodapp")
                }
            }
        }          
    }
}
   
