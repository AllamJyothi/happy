node('master')
{
    stage ('continuousdownload-master')
    {
        git 'https://github.com/selenium-saikrishna/maven1.git'
    }
    stage ('continuousbuild-master')
    {
        sh 'mvn package'
    }
    stage ('continuousdeployment-master')
    {
        sh 'sc /home/ubuntu/.jenkins/workspace/up_master/webapp/target/webapp.war ubuntu@172.31.0.130:/var/lib/tomcat7/webapps/qeen.war'
    }
}
  
  
  
  
  
  
  
  

