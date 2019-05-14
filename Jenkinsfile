node {
	   environment {
	     PATH = 'C:\\Program Files\\Git\\bin'
	   stage('SCM Checkout'){
	     git 'https://github.com/ismehene/HelloWorld'
	   }
           agent any triggers { pollSCM('* * * * *') }
	   stage('Compile-Package'){
	      //Get maven home path
	      def mvnHome = tool name: 'C:\\Program Files\\maven 3.3.9', type: 'maven'
	      bat "${mvnHome}/bin/mvn package"
	   }} 
