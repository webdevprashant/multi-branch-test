// pipeline {
//    agent any
//    stages {
//        stage('Build Code') {
//            steps {
//                sh """
//                echo "Building Artifact from Develop branch"
//                """
//            }
//        }
//       stage('Deploy Code') {
//           steps {
//                sh """
//                echo "Deploying Code from Develop branch"
//                """
//           }
//       }
//    }
// }

pipeline {
    agent any
    stages {
        stage('Master Branch Deploy Code') {
            when {
                branch 'master'
            }
            steps {
                sh """
                echo "Building Artifact from Master branch"
                """

                sh """
                echo "Deploying Code from Master branch"
                """
            }
        }
        stage('Develop Branch Deploy Code') {
            when {
                branch 'develop'
            }
            steps {
                sh """
                echo "Building Artifact from Develop branch"
                """
                sh """
                echo "Deploying Code from Develop branch"
                """
           }
        }
    }
}
