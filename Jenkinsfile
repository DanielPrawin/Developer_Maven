@Library("myLibrary")_
pipeline
{
    agent any
    stages
    {
        stage('Continious-Download')
        {
            steps
            {
                script
                {
                    try
                    {
                         cici.newGit("maven")
                        
                    }
                   catch(Exception e1)
                   {
                       
                   }
                }
            }
        }
        stage('Continious-Build')
        {
            steps
            {
                script
                {
                    try
                    {
                      cici.buildProcess()
                    }
                   catch(Exception e2)
                   {
                       
                   }
                }
            }
        }
        stage('Continious-download')
        {
            steps
            {
                script
                {
                    try
                    {
                       
                        cicd.deployment("Declarative_PipeLine","172.31.17.18","testapp2")
                    }
                   catch(Exception e3)
                   {
                       
                   }
                }
            }
        }
         stage('Continious-testing')
        {
            steps
            {
                script
                {
                    try
                    {
                        cici.newGit("FunctionalTesting")
                        cicd.testing("Declarative_PipeLine")
                    }
                   catch(Exception e4)
                   {
                       
                   }
                }
            }
        }
        stage('Continious-Delivery')
        {
            steps
            {
                script
                {
                    try
                    {
                       cicd.deployment("Declarative_PipeLine","172.31.18.195","prodapp2")
                        
                    }
                   catch(Exception e5)
                   {
                       
                   }
                }
            }
        }
    }
}
