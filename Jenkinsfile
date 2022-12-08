pipeline {
 agent {
   label {
           label 'built-in'
           customWorkspace "/data/vel-app"
}
}

   stages {
             stage ('install-apache') {
                 steps {
                       sh "service httpd start"
                    }
              }


             stage ('server-start') {
                     steps {
                         sh "service httpd start"
                       }
               }

          stage ('deploy-index') {
             steps {
                  sh "cp -r index.html /var/www/html"
                 sh "chmod -R 777 /var/www/html/index.html"
              }
          }
       }
    }
