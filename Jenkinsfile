node {

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    stage('Code Quality')
    {

        def msbuild = tool name: 'MSBuild', type: 'hudson.plugins.sonar.MsBuildSQRunnerInstallation'
    
            bat "\"${msbuild}\"\\SonarQube.Scanner.MSBuild.exe begin /k:demo123 /n:demo /d:sonar.host.url=http://localhost:9000 /d:sonar.login=dbd529efca4c5cf0dccf3922e67ca4f95183d05a /d:sonar.verbose=true"
            bat "'C:\\Program Files (x86)\\MSBuild\\14.0\\Bin\\MSBuild.exe' /t:Rebuild"
            bat "\"${msbuild}\"\\SonarQube.Scanner.MSBuild.exe end"
    
   }
}
