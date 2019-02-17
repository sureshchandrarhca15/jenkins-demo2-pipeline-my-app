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
      mail bcc: '', body: '''Hi, This is a Jenkins Email Notification
      Thanks
      Hari''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job Notification', to: 'sureshchand.rhce@gmail.com'
   }

}

