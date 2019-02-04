node('master')
{
    stage ('continuousdownload-test')
    {
        git 'https://github.com/selenium-saikrishna/maven1.git'
    }
    stage ('continuousbuild-test')
    {
        sh 'mvn package'
    }
    stage ('continuousdeployment-test')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/multibranch_test/webapp/target/webapp.war ubuntu@172.31.44.54:/var/lib/tomcat7/webapps/quit.war'
    }
    stage ('continuoustesting-test')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
    stage ('continuousdelivery-test')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/multibranch_test/webapp/target/webapp.war ubuntu@172.31.44.197:/var/lib/tomcat7/webapps/prodenv.war'
    }
}
  
  
  
  
  
  
  
  

