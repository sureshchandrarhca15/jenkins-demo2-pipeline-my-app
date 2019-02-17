  node{
   stage('SCM Checkout'){
     
     git 'https://github.com/sureshchandrarhca15/jenkins-demo2-pipeline-my-app.git'
   }
   stage('Compile-Package'){
    //Get Maven Home path
      def mvnHome =  tool name: 'maven_3_5_2', type: 'maven'   
     sh "${mvnHome}/bin/mvn clean install package -Dmaven.test.skip=true"
   }
    
   stage('Email Notification'){
    mail bcc: '', body: '''Hi,
    The Build Pipeline for "jenkins-demo2-pipeline-my-app" Job has been triggered Successfully. 

  Thanks,
  Jenkins Team''', cc: 'sureshchandra.rhca@gmail.com', from: '', replyTo: '', subject: 'Jenkins Email Notification', to: 'sureshchand.rhce@gmail.com'

   }

}

