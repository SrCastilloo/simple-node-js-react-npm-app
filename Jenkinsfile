pipeline {
agent {
docker {
image 'node:22-alpine' // Imagen de Docker
args '-p 3000:3000' // Puertos
}
}
stages {
stage('Build') {
steps {
sh 'npm install' // Instalar dependencias
}
}

stage('Test') {
steps {
sh './jenkins/scripts/test.sh'
}
}

stage('Deliver') {
steps {
sh './jenkins/scripts/deliver.sh'
input message: 'Finished using the web site? (Click "Proceed" to continue)'
sh './jenkins/scripts/kill.sh'
}
}


}
}