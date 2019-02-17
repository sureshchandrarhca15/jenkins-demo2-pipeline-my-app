  node{
   stage('SCM Checkout'){
     git 'https://github.com/sureshchandrarhca15/jenkins-demo2-pipeline-my-app.git'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'maven_3_5_2', type: 'maven'   
      sh 'mvn package'
   }
}

