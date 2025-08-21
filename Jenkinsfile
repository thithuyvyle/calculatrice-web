pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Démarrage du build...'
      }
    }
    stage ('Test') {
      steps { 
        script { 
           bat '''
              if exist index.html (
                  echo Le fichier index.html existe.
              ) else (
                  echo ERREUR : Le fichier index.html est introuvable !
                  exit /b 1
              )
           '''
        }
      }
    }
  }
}
