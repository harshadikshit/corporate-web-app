node {
    stage ('Checkout') { checkout scm }

    stage('upload-site-to-s3-bucket-wwwvalueblockio') {		
	withAWS(region:'eu-west-1', credentials:'jenkinss3uploader') {
		
		s3Upload(file:'public/dist/index.html', bucket:'wwwvalueblockio', path:'index.html', acl:'PublicRead')			
		s3Upload(file:'public/dist/theme.js', bucket:'wwwvalueblockio', path:'theme.js', acl:'PublicRead')
		s3Upload(file:'public/dist/theme.css', bucket:'wwwvalueblockio', path:'theme.css', acl:'PublicRead')

		s3Upload(file:'public/dist/app.bundle.js', bucket:'wwwvalueblockio', path:'app.bundle.js', acl:'PublicRead')
		s3Upload(file:'public/dist/app.css', bucket:'wwwvalueblockio', path:'app.css', acl:'PublicRead')			
	}	
   } 
}
