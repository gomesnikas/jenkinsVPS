pipeline 
    agent any
    
    stages {
        stage('déploement production') {
            matrix {
                axes{
                    axis {
                        name 'PLATEFROM'
                        values 'Linux', 'MacOs', 'windows'
                    }
                    axis {
                        name 'BROWSER'
                        values 'Chrome', 'Firefox', 'Safari'
                    }
                }
                stages {
                    stage('build') {
                        steps {
                            echo "construire pour ${ PLATEFORM } - ${ BROWSER}"
                        }
                    stage('test') {
                        steps {
                            echo "test pour ${ PLATEFORM } - ${ BROWSER }"
                        }
                    }    
                }
            }
        }
    }
}