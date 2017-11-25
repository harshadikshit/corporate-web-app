node {
    stage ('Checkout') { checkout scm }

    stage('upload-site-to-s3-bucket-wwwvalueblockio') {		
	withAWS(region:'eu-west-1', credentials:'jenkinss3uploader') {
		s3Upload(file:'index.html', bucket:'wwwvalueblockio', path:'index.html', acl:'PublicRead')			
	}	
   } 
}
