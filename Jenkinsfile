pipeline {

             agent {

                 label {

               label "built-in"
              
           }
        }
     
               stages {

                    stage ("deploy") {
            
            steps {
               sh "docker run -dp 70:80 --name a4 httpd"
               sh "docker cp index.html a4:/usr/local/apache2/htdocs/index.html"
              sh "docker exec a4 chmod -R 755 /usr/local/apache2/htdocs/"
            }
        }


       }

          }
