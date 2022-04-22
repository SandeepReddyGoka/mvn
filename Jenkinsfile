node('built-in') 
   {
    stage('continuous download') 
          {
            git 'https://github.com/SandeepReddyGoka/mvn.git'
          }
    stage('continuous build')
          {
            sh 'mvn package'
          }
    stage('continuous deployment')
          {
            sh 'scp /home/ubuntu/.jenkins/workspace/samplepipeline/target/webappgoogle-1.0-SNAPSHOT.war
            ubuntu@172.31.3.150:/var/lib/tomcat9/webapps/qaenv.war'
          }
    stage('continuous testing')
          {
            sh 'echo "Testing Passed"'
          }
    stage('continuous delivery')
          {
            sh 'scp /home/ubuntu/.jenkins/workspace/samplepipeline/target/webappgoogle-1.0-SNAPSHOT.war 
            ubuntu@172.31.6.36:/var/lib/tomcat9/webapps/prodenv.war'
  }