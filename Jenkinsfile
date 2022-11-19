pipeline {
    agent any;
  stages {

    stage ('BUILD') {
      steps {
        echo "This is Build stage" 
        sh ''' echo $BUILD_NUMBER
               echo $BUILD_ID  
           '''
     
      }  
    }  
    
    stage ('TEST') {
      parallel{
      
         stage('QA'){
             steps {
                   echo "This is QA stage" 
             }
         }
         stage('BVT'){
             steps {
                   echo "This is BVT stage" 
             }
         }    
       
      } 
    }  
    
    stage ('DEPLOY') {
        steps {
             echo "This is Deploy stage" 
             sh 'sleep 5'
        }
   }
        
  }

}
