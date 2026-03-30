pipeline {

             agent {

                 label {

               label "built-in"
              
           }
        }
     
               stages {

                    stage ("deploy") {
            
            steps {
               sh "docker run -dp 70:80 --name a5 httpd"
               sh "docker cp index.html a5:/usr/local/apache2/htdocs/index.html"
              sh "docker exec a5 chmod -R 755 /usr/local/apache2/htdocs/"
            }
        }


       }

          }
