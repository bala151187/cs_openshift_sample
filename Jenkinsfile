node {


    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    stage('Code Quality')
    {
   
        def msbuild = tool name: 'MSBuild', type: 'hudson.plugins.sonar.MsBuildSQRunnerInstallation'
        bat "\"${msbuild}\SonarQube.Scanner.MSBuild.exe" example.sln"
  }

}
