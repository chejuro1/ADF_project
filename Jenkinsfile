node('pwsh') {
    stage('Checkout') {
        checkout scm
    }
    stage('Build'){
        container('pwsh') {
            // This is where we build our code.
        }
    }
}
