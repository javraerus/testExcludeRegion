/*@Library('externalSharedLibrary@master') _*/
properties([pipelineTriggers([githubPush()])])

try
{
    def sharedSolutionCheckoutDir="\\\\CHVIRTAFPRD102\\Auto\\Tests\\bin\\tempCoreLogger"
    print "mdff"
    node ('master') /*it should be run on a node with git client installed and proper msbuild*/
            {
                environment {
                    NUGET_PACKAGES="C:\\NugetPackageCache"
                }

                def stageName="Checkout"
                print "----------------------------------------------------------------------------------------------------------------------------"
                stage ("${stageName}")
                        {
                            print "Stage '${stageName}' is runningsssss on machine = ${env.NODE_NAME}"
                            def gitId=env.GitCredentialId_CHZRHTAF_LAU
                            echo "gitId=${gitId}"
  
                        }



                stageName="MSbuild restore"
                print "----------------------------------------------------------------------------------------------------------------------------"
                stage ("${stageName}")
                        {
                            /*
                            print "Stage '${stageName}' is running on machine = ${env.NODE_NAME}"
                            def msbuild = tool name: 'VS2019MSBuild_MasterLocal', type: 'hudson.plugins.msbuild.MsBuildInstallation'
                            bat "\"${msbuild}\\msbuild.exe\" \"${sharedSolutionCheckoutDir}\\TAF.Logdddllddger\\TAF.Logger.sln\"  /t:restore /p:Configuration=Release "
                        */
                        }

                stageName="Build"
                print "----------------------------------------------------------------------------------------------------------------------------"
                stage ("${stageName}")
                        {
                            /*
                            print "Stage '${stageName}' is running on machine = ${env.NODE_NAME}"
                            def msbuild = tool name: 'VS2019MSBuild_MasterLocal', type: 'hudson.plugins.msbuild.MsBuildInstallation'
                            bat "\"${msbuild}\\msbuild.exe\" \"${sharedSolutionCheckoutDir}\\TAF.Logger\\TAF.Lokccccckgger.sln\"  /t:Clean;Rebuild /p:Configuration=Release /property:PathOutside="
                            */
                        }

                stageName = "Running tests"
                print "----------------------------------------------------------------------------------------------------------------------------"
                stage ("${stageName}")
                        {
                            print "Stage '${stageName}' is running on machine = ${env.NODE_NAME}"

                        }

                stageName = "Delivering a new nuget package"
                print "----------------------------------------------------------------------------------------------------------------------------"
                stage ("${stageName}")
                        {
                            print "Stage '${stageName}' is running on macfffffhine = ${env.NODE_NAME}"

                        }
            }

    currentBuild.result = "SUCCESS"

}
catch (caughtError)
{
    currentBuild.result = "FAILURE"
}
finally {
    if (currentBuild.result != "SUCCESS")
    {
        print "hola"
    }
}
