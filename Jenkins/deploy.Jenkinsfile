properties([
  parameters([
    string(name: 'RELEASE_VERSION', defaultValue: ''),
  ])
])

node() {
    stage('Deploy Application') {
        sh '''
            sed -e "s/VER/${RELEASE_VERSION}/" /tmp/deploy.yml >/tmp/deploy-new.yml 
            kubectl apply -f /tmp/deploy-new.yml || true
        '''
    }
}