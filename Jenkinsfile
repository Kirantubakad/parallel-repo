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
        parallel{
            stage('SERVER1'){   
               steps {
                  echo "This is server1 Deploy stage" 
                  sh 'sleep 5'
               }
            }
            stage('SERVER2'){   
               steps {
                  echo "This is server2 Deploy stage" 
                  sh 'sleep 5'
               }
            }
            stage('SERVER3'){   
               steps {
                  echo "This is server3 Deploy stage" 
                  sh 'sleep 5'
               }
            }
            stage('SERVER4'){   
               steps {
                  echo "This is server4 Deploy stage" 
                  sh 'sleep 5'
               }
            }
        }
    }
 }
}
