node {
  def remote = [:]
  remote.name = 'DigitalOcean'
  remote.host = '134.209.97.202'
  remote.user = 'root'
  remote.password = 'y2023-artcode@System'
  remote.allowAnyHosts = true
  stage('Remote SSH') {
    sshCommand remote: remote, command: "ls -lrt"
    sshCommand remote: remote, command: "cd /sample-cicd/sample-ci-cd-backend"
    sshCommand remote: remote, command: "pwd"
  }
}