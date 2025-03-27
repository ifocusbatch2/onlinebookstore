node{
       stage('clone the project'){
       
           git branch: 'feature/2025.03.27', url: 'https://github.com/ifocusbatch2/onlinebookstore.git'
         
         
		 
       }

       stage('Build the project'){
   
           sh 'mvn clean install'
        }

       

       stage('Test'){
      
           sh 'mvn test'
        
       }
       stage('published the test results'){
     
           junit 'target/surefire-reports/*.xml'
        

       }
       stage('publishedd the artifacts'){

           archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
        

       }

    }
