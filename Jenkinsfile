@Library("myLibrary")_
pipeline
{
    agent any
    stages
    {
        stage('continious download')
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
                    exit(1)
                }
                }
            }
        }
         stage('continious built')
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
                    exit(2)
                }
                }
            }
        }
         
         stage('continious deploy')
        {
            steps
            {
                script
                {
                    
                try
                {
                   cicd.deploy("ScriptedPipeLine","172.31.47.214","testapp11");
                }
                catch(Exception e3)
                {
                    exit(3)
                }
                }
            }
        }
         stage('continious testing')
        {
            steps
            {
                script
                {
                    
                try
                {
                  cicd.newGit("Tester");
                  cicd.testing("testing");
                }
                catch(Exception e4)
                {
                    exit(4)
                }
                }
            }
        }
          stage('continious delivery')
        {
            steps
            {
                script
                {
                    
                try
                {
                    cicd.deploy("ScriptedPipeLine","172.31.42.212","prodapp12");
                }
                catch(Exception e5)
                {
                    exit(5)
                }
                }
            }
        }
    }
}
