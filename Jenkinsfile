pipeline {
    agent any

    stages {
        stage('Configure Git') {
            steps {
                bat 'git config --global --add safe.directory "C:/Users/NASHATH V N/Downloads/flutter_windows_3.47.4-stable/flutter"'
            }
        }

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
                bat '''
                set ANDROID_HOME=C:\\Android\\Sdk
                set ANDROID_SDK_ROOT=C:\\Android\\Sdk
                "C:\\Users\\NASHATH V N\\Downloads\\flutter_windows_3.47.4-stable\\flutter\\bin\\flutter.bat" config --android-sdk C:\\Android\\Sdk
                "C:\\Users\\NASHATH V N\\Downloads\\flutter_windows_3.47.4-stable\\flutter\\bin\\flutter.bat" doctor
                "C:\\Users\\NASHATH V N\\Downloads\\flutter_windows_3.47.4-stable\\flutter\\bin\\flutter.bat" build apk --release
                '''
            }
        }
    }
}