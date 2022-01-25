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
                    cicd.newgit("https://github.com/lalitha419/kpmaven.git")
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
	}
	}
