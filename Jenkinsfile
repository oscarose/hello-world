node {
     //stage('checkout scm') {
         //git url: 'https://github.com/oscarose/hello-world.git'
         //credentialsId: 'Github'
     //}
     stage('import') {
          withEnv(["PATH+ANSIBLE=${tool 'ansible'}"]) {
          sh 'echo $PATH'
            sh 'ls -altr'
            sh 'ansible --version'
            sh 'which ansible'
            sh 'ansible-playbook -i "${Server_IP}," -k -b --extra-vars "app_user=${app_user} artifactory_user=${artifactory_user} artifactory_password=${artifactory_password} ansible_ssh_pass=${ssh_pwd} ansible_become_pass=${ssh_pwd} tomcat_version=${tomcat_version} install_dir=${install_dir} jenkins_dir=${jenkins_dir} java_name=${java_name} Server_IP=${Server_IP}" ${WORKSPACE}/myrepo/$Ansible_Playbook '
          }
     }
}

