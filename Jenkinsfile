pipeline {
   agent { label "master" }
   stages { 
      stage("build"){
      steps { 
         bat "docker build -t apipeliculas ."
      }
   }
   
   stage("run") { 
      steps { 
         bat "docker run --rm -d  -p 8080:5000/tcp apipeliculas:latest <"
      }
   }

   }

}