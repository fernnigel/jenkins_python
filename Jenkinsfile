node {
  stage("Clone the project") {
    git branch: 'main', url: 'https://github.com/fernnigel/jenkins_python.git'
  }
  stage("Setting Virtual Environment") {
        sh 'python -m venv .'
  }
  stage("Installing") {
     sh './bin/pip install -r requirement.txt'
  }
  stage("Deploying") {
    sh 'python app1.py'
  }
  stage("Notifying") {
    emailext body: 'Deployed Successfully' , 
        subject: 'App Deployed Status' , 
        to: 'nigelfernandes.contact@gmail.com'
  }
}