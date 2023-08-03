@Library("myLibrary")_
pipeline
{
    agent any
    stages
    {
        stage('continious-download')
        {
            steps
            {
                script
                {
                    try
                {
                    cicd.newGit("Developer_Maven")
                }
                catch(Exception e3)
                {
                    
                }
                }
                
            }
        }
         stage('continious-built')
        {
            steps
            {
                script
                {
                    try
                {
                   cicd.buildwar()
                }
                catch(Exception e4)
                {
                    
                }
                }
                
            }
        }
         stage('continious-deploy')
        {
            steps
            {
                script
                {
                    try
                {
                    cicd.depoly("ScriptedPipeLine","172.31.24.2","testapp5")
                }
                catch(Exception e3)
                {
                    
                }
                }
                
            }
        }
        stage('continious-testing')
        {
            steps
            {
                script
                {
                    try
                {
                      cicd.newGit("Tester")
                      cicd.testing("ScriptedPipeLine")
                }
                catch(Exception e4)
                {
                    
                }
                }
                
            }
        }
        stage('continious-delivery')
        {
            steps
            {
                script
                {
                    try
                {
                    cicd.depoly("ScriptedPipeLine","172.31.20.239","prodapp5")
                }
                catch(Exception e5)
                {
                    
                }
                }
                
            }
        }
       
    }
}
