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
                        cicd.newGit("Developer_Maven");
                    }
                    catch(Exception e1)
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
                      cicd.build();
                    }
                    catch(Exception e2)
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
                        cicd.copyBuilt("ScriptedPipeLine","172.31.3.227","testapp2");
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
                        cicd.newGit("Tester");
                        cicd.test("ScriptedPipeLine");
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
                     
                        cicd.copyBuilt("ScriptedPipeLine","172.31.5.152","prodapp2");
                    }
                    catch(Exception e5)
                    {
                        
                    }
                }
            }
        }
    }
}
