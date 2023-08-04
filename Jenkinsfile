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
                        cicd.newGit("Developer_Maven");
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
                      cicd.build();
                    }
                    catch(Exception e2)
                    {
                        
                    }
                }
             }
        }
        stage('Continious-Deployment')
        {
            steps
             {
                script
                {
                    try
                    {
                        cicd.deploy("ScriptedPipeLine","172.31.16.8","testapp2");
                    }
                    catch(Exception e2)
                    {
                        
                    }
                }
             }
        }
        stage('Continious-Testing')
        {
            steps
             {
                script
                {
                    try
                    {
                         cicd.newGit("Tester");
                        cicd.testing("ScriptedPipeLine")
                    }
                    catch(Exception e2)
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
                        cicd.deploy("ScriptedPipeLine","172.31.21.25","prodapp2");
                    }
                    catch(Exception e2)
                    {
                        
                    }
                }
             }
        }
    }
}
