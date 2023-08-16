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
                         cicd.newgit("Developer_Maven");
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
                        cicd.built();
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
                        cicd.deploy("ScriptedPipeLine","172.31.1.188","testapp2")
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
                        cicd.newgit("Tester");
                        cicd.testing("ScriptedPipeLine");
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
                      cicd.deploy("ScriptedPipeLine","172.31.2.82","prodapp2")
                     }
                     catch(Exception e5)
                     {
                         
                     }
                }
            }
        }
    }
}
