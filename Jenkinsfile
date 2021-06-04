pipeline {
   agent { label "linux" }
   stages { 
      steps { 
         sh "docker build -t apipeliculas ."
      }
   }
   stage("run") { 
      steps { 
         sh "docker run --rm -d  -p 8080:5000/tcp apipeliculas:latest <"
      }
   }

}