node {


    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }
    stage('Code Quality')
    {
    bat "\"${env.msbuild}\" ".\"example.sln"   
    }

}
