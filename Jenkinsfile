node {


    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    stage('Code Quality')
    {
        SonarQube.Scanner.MSBuild.exe begin //k:"demo" \/d:sonar.host.url="http://localhost:9000" \/d:sonar.login="dbd529efca4c5cf0dccf3922e67ca4f95183d05a"
        MsBuild.exe //t:Rebuild
        SonarQube.Scanner.MSBuild.exe end //d:sonar.login="dbd529efca4c5cf0dccf3922e67ca4f95183d05a"
    }

}
