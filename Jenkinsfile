## android-sample-app
sample android app which integrates the datatrans library

![app screenshots](/static/datatrans-android-sample-app-screenshots.png)

### Build & Installation
```bash
$ ./gradlew assemble
$ adb install -r app/build/outputs/apk/app-debug.apk
```
### APK
[datatrans-android-sample.apk](https://github.com/datatrans/android-sample-app/raw/master/static/datatrans-android-sample.apk)

### Documentation
- [Dev guide](https://admin.sandbox.datatrans.com/showcase/doc/Android_Developers_Manual.pdf)
- [Release notes](https://admin.sandbox.datatrans.com/showcase/doc/Android_Release_Notes.pdf)

Note: Please don't use the code from this sample in production.
# Andriod-test-


/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent any
    environment {
        ANDROID_HOME = '/usr/lib/android-sdk'  // Verify this path matches your installation!
    }
    stages {
        stage('Accept Licenses') {
            steps {
                sh '''
          yes | ${ANDROID_HOME}/cmdline-tools/latest/bin/sdkmanager --licenses
        '''
            }
        }
        stage('Install SDK Tools') {
            steps {
                sh '''
          ${ANDROID_HOME}/cmdline-tools/latest/bin/sdkmanager --sdk_root=${ANDROID_HOME} "platform-tools" "platforms;android-34"
        '''
            }
        }
        stage('Build') {
            steps {
                sh './gradlew assembleDebug'
            }
        }
    }
}
 
