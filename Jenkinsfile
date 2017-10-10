node {
    stage 'Checkout' { checkout scm }

	stage('compile') { withMaven(maven: 'Maven-3-5-0') { sh "mvn clean install" } }   
}