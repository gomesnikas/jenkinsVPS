pipeline {
    agent any

    stages {
        stage('déploement production') {
            matrix {
                axes {
                    axis {
                        name 'PLATFORM'
                        values 'Linux', 'MacOS', 'Windows'
                    }
                    axis {
                        name 'BROWSER'
                        values 'Chrome', 'Firefox', 'Safari'
                    }
                }
                stages {
                    stage('build') {
                        steps {
                            echo "Construire pour ${PLATFORM} - ${BROWSER}"
                        }
                    }
                    stage('test') {
                        steps {
                            echo "Test pour ${PLATFORM} - ${BROWSER}"
                        }
                    }
                }
            }
        }
    }
}
