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
        sh 'scp /home/ubuntu/.jenkins/workspace/multibranch_test/webapp/target/webapp.war ubuntu@/var/lib/tomcat172.31.14.183/webapps/qeen.war'
    }
}
  
  
  
  
  
  
  
  

