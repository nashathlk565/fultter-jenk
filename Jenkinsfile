pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                bat '"C:\\Users\\NASHATH V N\\Downloads\\flutter_windows_3.47.4-stable\\flutter\\bin\\flutter.bat" pub get'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\NASHATH V N\\Downloads\\flutter_windows_3.47.4-stable\\flutter\\bin\\flutter.bat" test'
            }
        }

        stage('Build APK') {
            steps {
                bat '"C:\\Users\\NASHATH V N\\Downloads\\flutter_windows_3.47.4-stable\\flutter\\bin\\flutter.bat" build apk --release'
            }
        }
    }
}