node {
    stage('Checkout') {
        checkout scm
    }

    stage('Install requirements') {
        sh 'pip install -r requirements.txt'
    }

    stage('Run tests') {
        sh 'pytest --maxfail=1 --disable-warnings -q'
    }

    stage('Post Clean') {
        cleanWs()
    }
}
