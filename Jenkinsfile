pipeline{
  
  // this section is not mandatory
      // tools that we have configured
  tools{
      
      maven 'mymaven'
  }
    // agent = server where the pipeline has to run
    // here any = any available server which jenkisn is connected to - Lab server
    // agent is mandatory section
    agent any
    
    // this is a mandatory section -> what should pieplien execute
    // stages -> what jobs to run
    stages{
        
        // Stage= A job
        stage('Clone Code')
        {
           steps{
               git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
           } 
        }
        stage('Compile Code')
        {
            steps{
                sh 'mvn compile'
            }
        }
        
         stage('Review Code')
        {
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        
         stage('Test Code')
        {
            steps{
                sh 'mvn test'
            }
        }
        
         stage('Build Code')
        {
            steps{
               
               sh 'mvn package' 
            }
        }
        
    }
}
