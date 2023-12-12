pipeline {
environment{
   registry ='snehal01102002/assi10'
   registryCredent = 'docker_id'
   dockerImage= ''
}
   agent any 
   stages {
      stage ('Build image')
      {
         steps{
            script{
               dockerImage = docker.build registry + ":$BUILD_NUMBER"
            }
         }
      }
      //stage( 'Deploy the image')
      // {
           //steps{
              // script {
                  //docker.withRegistry( '', registryCredintial )
                 // {
                    // docker.Image.push()
                  //}
               //}
            }
         }
         // stage('Clenaing up'){
       //  steps{
       //     bat "docker rmi $registry:$BUILD_NUMBER"
         //}
    //  }
  // }
//}



               
               
