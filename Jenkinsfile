node {
    
    stage('Preparation') {
        
        git 'https://github.com/sandu1011/fleetman-webapp'
    }
    stage('Build') {
        sh "mvn package"
    }
    stage('Results') {
        
        junit '**/target/surefire-reports/TEST-*.xml'
        archive 'target/*.jar'
    }

}
