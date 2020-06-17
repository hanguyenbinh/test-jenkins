pipeline {
   agent any

   stages {
       
        stage('Remote SSH') {
            steps{
                script{
            def remote = [:]
        remote.name = "hostname"
        remote.host = "202.134.19.247"
        remote.port = 22
        remote.user = "altisss_binh"
        remote.password = 'qfwHpjFLOR2tmkkCQyAK'
        remote.allowAnyHosts = true
         sshCommand remote: remote, command: 'ls && test -d "/home/altisss_binh/test-jenkins" && echo "test-jenkins existed" || git clone https://github.com/hanguyenbinh/test-jenkins.git'
            sshCommand remote: remote, command: "ls -lrt && cd test-jenkins && npm install && node index.js"
            }
            }
            
            
           
        }
   }
}
