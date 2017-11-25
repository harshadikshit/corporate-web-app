node {
    stage ('Checkout') { checkout scm }

    stage('upload-site-to-s3-bucket-wwwvalueblockio') {		
	withAWS(region:'eu-west-1', credentials:'jenkinss3uploader') {
		s3Upload(file:'index.html', bucket:'wwwvalueblockio', path:'index.html', acl:'PublicRead')
		s3Upload(file:'css', bucket:'wwwvalueblockio', path:'css', acl:'PublicRead')
		s3Upload(file:'img', bucket:'wwwvalueblockio', path:'img', acl:'PublicRead')
		s3Upload(file:'js', bucket:'wwwvalueblockio', path:'js', acl:'PublicRead')
		s3Upload(file:'vendor', bucket:'wwwvalueblockio', path:'vendor', acl:'PublicRead')
		s3Upload(file:'scss', bucket:'wwwvalueblockio', path:'scss', acl:'PublicRead')			
	}	
   } 
}
