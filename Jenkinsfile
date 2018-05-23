node {


    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    stage('Code Quality')
    {
   
        def msbuild = tool name: 'C:\\Program Files (x86)\\Jenkins\\tools\\hudson.plugins.sonar.MsBuildSQRunnerInstallation\\MSBuild', type: 'hudson.plugins.sonar.MsBuildSQRunnerInstallation'
        bat "${msbuild} example.sln"
  }

}
