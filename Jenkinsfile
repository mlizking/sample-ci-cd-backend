node {
  def remote = [:]
  remote.name = 'DigitalOcean'
  remote.host = '134.209.97.202'
  remote.user = 'root'
  remote.password = 'y2023-artcode@System'
  remote.allowAnyHosts = true
  stage('Remote SSH') {
    sshCommand remote: remote, command: "ls -lrt"
    sshCommand remote: remote, command: "for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done"
  }
}