node {
  checkout scm
  
  stage("Get Package") {
      sh '''
      echo "Hello!"
        wget -q -O - https://packages.cloudfoundry.org/debian/cli.cloudfoundry.org.key | sudo apt-key add -
        echo "deb https://packages.cloudfoundry.org/debian stable main" | sudo tee /etc/apt/sources.list.d/cloudfoundry-cli.list
       '''
  }
  stage("Update") {
      sh '''
      echo "Hello!"
        sudo apt-get update -y
        '''
  }
  stage("Install CLI") {
      sh '''
      echo "Hello!"
        sudo apt-get install cf-cli -y
        '''
  }
  stage("Verify Install") {
      sh '''
      echo "Hello!"
        cf --help
        '''
  }
}
