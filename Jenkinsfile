node('pwd') {
    stage('Checkout') {
        checkout scm
    }
    stage('Build'){
        container('pwd') {
            // This is where we build our code.
        }
    }
}
