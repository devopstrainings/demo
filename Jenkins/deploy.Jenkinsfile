properties([
  parameters([
    string(name: 'RELEASE_VERSION', defaultValue: ''),
  ])
])

node() {
    stage('Deploy Application') {
        sh '''
            sed -e "s/VER/${params.RELEASE_VERSION}/" /tm
        '''
    }
}