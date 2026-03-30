pipeline {

             agent {

                 label {

               label "built-in"
              
           }
        }
     
               stages {

                    stage ("deploy") {
            
            steps {
               sh "docker run -dp 9080:80 --name a2 httpd"
               sh "docker cp index.html a1:/usr/local/apache2/htdocs/index.html"
              sh "docker exec a1 chmod -R 755 /usr/local/apache2/htdocs/"
            }
        }


       }

          }
