
node {

   def mvn = tool (name: 'maven3', type: 'maven') + '/bin/mvn'
   stages {
          stage('Checkout SCM') {
            steps {
                checkout([
                 $class: 'GitSCM',
                 branches: [[name: 'master']],
                 userRemoteConfigs: [[
                    url: 'https://github.com/ek2020/devops-training.git',
                    credentialsId: '',
                 ]]
                ])
            }
        }
   
   stage('compile-package')
   {
      sh '${mvn}/bin/mvn package'
   }
   }
      

//   stage('Mvn Package'){
	   // Build using maven
	   
	//   sh "${mvn} clean package deploy"
   //}
   
   
}

