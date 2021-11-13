pipeline {
 agent any 

	stages {
				
		stage ('Creating a Bucket') {
			steps {
			bat 'gsutil mb -p sivaramgcp -c nearline -l us-east1 -b on gs://pipelinebucket'
			
			}
		}

		stage ('list the buckets') {
			steps {
			bat 'gsutil ls'
			}
		}
		stage ('To Display the size of bucket') {
			steps {
			bat 'gsutil du -s gs://pipelinebucket'
			}
		}
		
		stage ('To Display Bucket Metadata') {
			steps {
			bat 'gsutil ls -L -b gs://pipelinebucket'
			}
		}
		stage ('To List the Objects in Bucket') {
			steps {
			bat 'gsutil ls -r gs://pipelinebucket'
			}
		}
		
		stage ('To copy the Objects in Bucket') {
			steps {
			bat 'gsutil cp  gs://siva-simple-bucket/dsktp.jpg  gs://pipelinebucket/dsktp1.jp'
			}
		}
	
	}
	}
