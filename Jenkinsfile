node {

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    stage('Code Quality')
    {

        def msbuild = tool name: 'MSBuild', type: 'hudson.plugins.sonar.MsBuildSQRunnerInstallation'
        withSonarQubeEnv('My SonarQube Server') {
            bat "\"${msbuild}\"\SonarQube.Scanner.MSBuild begin /k:'demo' /d:sonar.host.url='http://localhost:9000' /d:sonar.login='dbd529efca4c5cf0dccf3922e67ca4f95183d05a' example.sln"
            bat "\"${msbuild}\"\SonarQube.Scanner.MSBuild.exe end"
    }
   }
}
