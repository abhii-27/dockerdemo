pipeline {

             agent {

                 label {

               label "built-in"
               customWorkspace "/mnt/test4"
           }
        }
     
               stages {

                    stage ("deploy) {
            
            steps {
  
                docker ('default')

               sh "service httpd start"
               sh "docker run -dp 90:80 --name a1 httpd"
               sh "docker cp index.html a1:/usr/local/apache2/htdocs"

            }
        }


       }

          }
