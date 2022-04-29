node {
    stage('Checkout') {
        checkout scm
    }  
    stage('Package') {
       sh 'mvn package -DskipTests'
    }
    stage('Test') {
        sh 'mvn test'
    }
}



