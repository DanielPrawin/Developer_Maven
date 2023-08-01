@Library("myLibrary1")_
pipeline
{
    agent any
    stages
    {
        stage('C-download')
        {
          steps
          {
              script
              {
                  try
                  {
                      cicd.newGit("Developer_Maven")
                  }
                  catch (Exception e1)
                  {
                      
                  }
                  
              }
          }    
        }
         stage('C-built')
        {
          steps
          {
              script
              {
                   try
                  {
                       cicd.build()
                  }
                  catch (Exception e2)
                  {
                      
                  }
                 
              }
          }    
        }
        stage('C-deployment')
        {
          steps
          {
              script
              {
                   try
                  {
                         cicd.deployment("sp2","172.31.14.233","testapp2")
                  }
                  catch (Exception e3)
                  {
                      
                  }
               
              }
          }    
        }
        stage('C-testing')
        {
          steps
          {
              script
              {
                   try
                  {
                      cicd.newGit("Tester")
                      cicd.testscenario("sp2")
                  }
                  catch (Exception e4)
                  {
                      
                  }
                
              }
          }    
        }
        stage('C-delivery')
        {
          steps
          {
              script
              {
                   try
                  {
                      cicd.deployment("sp2","172.31.14.94","prodapp7")
                  }
                  catch (Exception e5)
                  {
                      
                  }
                  
              }
          }    
        }
    }
}
