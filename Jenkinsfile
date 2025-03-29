pipeline:
  agent: any
  triggers:
    - pollSCM: "H/2 * * * *"
  stages:
    - stage: "Checkout Code"
      steps:
        - sh: "git clone https://github.com/your-username/your-repo.git"
    - stage: "Build"
      steps:
        - sh: "mvn clean package"
    - stage: "Deploy to Tomcat"
      steps:
        - sh: "cp target/mywebapp.war /opt/tomcat9/webapps/"
        - sh: "/opt/tomcat9/bin/shutdown.sh || true"

