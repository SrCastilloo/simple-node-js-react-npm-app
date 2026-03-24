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
}
}