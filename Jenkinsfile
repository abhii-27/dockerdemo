pipeline {

             agent {

                 label {

               label "built-in"
              
           }
        }
     
               stages {

                    stage ("deploy") {
            
            steps {
               sh "docker run -dp 90:80 --name a1 httpd"
               sh "docker cp index.html a1:/usr/local/apache2/htdocs"
              sh "docker exec a1 chmod -R 755 /usr/local/apache2/htdocs/"
            }
        }


       }

          }
