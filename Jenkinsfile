pipeline {
             agent {
                 label {
               label "built-in"
               } 
        }
            environment{
              REPO_URL = " https://github.com/abhii-27/dockerdemo.git "
            }
                    stages {
                 stage ("CleanWorksc") {
                   steps {
                     cleanWs()
                   }
                 }   
                   stage ("DeployQ1branchC1") {
                   steps { 
                            dir("Q1") { 
                git branch:"2026Q1",url:"${Repo_URL}"
                sh" rm -rf a1 "
                sh "docker run -dp 9090:80 --name a1 httpd"
                sh "docker cp index.html a1:/usr/local/apache2/htdocs/index.html"
                sh "docker exec a1 chmod -R 755 /usr/local/apache2/htdocs/"                                           
                             }
                       }
                 }
                stage ("DeployQ2branchC2") {
                   steps { 
                            dir("Q2") { 
                git branch:"2026Q2",url:"${Repo_URL}"
                sh" rm -rf a2 "
               sh "docker run -dp 9090:80 --name a2 httpd"
               sh "docker cp index.html a2:/usr/local/apache2/htdocs/index.html"
               sh "docker exec a2 chmod -R 755 /usr/local/apache2/htdocs/"                                   
                              }
                       }
                 }
                 stage ("DeployQ3branchC3") {
                   steps { 
                            dir("Q3") { 
                git branch:"2026Q3",url:"${Repo_URL}"
                sh" rm -rf a3 "
               sh "docker run -dp 9090:80 --name a3 httpd"
               sh "docker cp index.html a3:/usr/local/apache2/htdocs/index.html"
               sh "docker exec a3 chmod -R 755 /usr/local/apache2/htdocs/"                                  
                              }
                       }
                 }     
        }
 }
