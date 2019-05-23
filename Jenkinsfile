def label = "mypod-${UUID.randomUUID().toString()}"
podTemplate(label: label, containers: [
    containerTemplate(name: 'npm', image: 'node:carbon-jessie', ttyEnabled: true, command: 'cat'),
    
  ]) {

    node(label) {
        stage('Get a npm project') {
            git 'https://github.com/jenkinsci/kubernetes-plugin.git'
            container('npm') {
                stage('Build a npm project') {
                    sh 'npm install'
                    sh 'npm test'
                }
            }
        }

    

    }
}