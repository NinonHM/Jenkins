node {
    stage('Checkout') {
        checkout scm
    }  
    stage('Package') {
        mvn package -D skipTests
    }
}



