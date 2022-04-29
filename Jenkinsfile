def VERSION
def TAGGED

node {
     
    stage('Package') {
       sh "mvn package -DskipTests"
    }
    stage('Test') {
        sh "mvn test"
    }

    stage('Checkout') {
        checkout scm
        if (env.TAG_NAME){
            TAGGED = true
            VERSION = env.TAG_NAME.substring(1)
            echo $(VERSION)
            
        } else {
            TAGGED = false
            VERSION = null
            echo 'snapshot'  
        }
    } 
}



