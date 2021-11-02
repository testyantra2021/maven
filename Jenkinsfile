
//#Edited on Feature branch
node('master') 
{
  stage('Continuous Download') 
  {
    git 'https://github.com/selenium-saikrishna/maven.git'
  }
      stage('Continuous Compile') 
    {
         sh label: '', script: 'mvn compile'
    }
  stage('Continuous Build') 
  {
    sh 'mvn package'
  } 
  //stage('ContinuousDeployment') 
  //{
    //sh 'scp /home/vagrant/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war vagrant@10.0.0.51:/var/lib/tomcat7/webapps/qaenv.war'
  //}
  //stage('ContinuousTesting') 
  //{
    //git 'https://github.com/selenium-saikrishna/TestingOnLinux.git'
    
  //}
  //stage('ContinuousDelivery') 
  //{
    //  input message: 'Waiting for approval !', submitter: 'Venu'
    //sh 'scp /home/vagrant/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war vagrant@10.0.0.52:/var/lib/tomcat7/webapps/prodenv.war'
  //}
  
  
    stage('Continuous Test') 
    {
         sh label: '', script: 'mvn test'
    }  
      stage('Continuous Verify') 
    {
         sh label: '', script: 'mvn verify'
    }
      stage('Continuous Install') 
    {
         sh label: '', script: 'mvn install'
    }
  
     /* stage('Continuous Site') 
    {
         sh label: '', script: 'mvn site'
    }*/
  
}
