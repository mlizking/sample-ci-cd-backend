node {
  def remote = [:]
  remote.name = 'DigitalOcean'
  remote.host = '134.209.97.202'
  remote.user = 'root'
  remote.password = 'y2023-artcode@System'
  remote.allowAnyHosts = true
  stage('Remote SSH') {
    sshCommand remote: remote, command: "echo 'Hello From SERVER!!'"
  }
  stage('Pull Latest') {
    sshCommand remote: remote, command: "cd sample-cicd/sample-ci-cd-backend && git checkout develop && git pull"
  }
  stage('Build & Deploy') {
    sshCommand remote: remote, command: "cd sample-cicd/sample-ci-cd-backend && docker-compose down && docker rmi samplecicdbackend_backend && docker-compose up -d"
  }
}