node {
	stage ('Git SCM') {

		git 'https://github.com/Kapombo/WebGoat-Legacy.git'

	}
	stage ('Show PATH') {
			 environment {
    PATH = "/usr/lib/jvm/java-1.8.0-openkdj-amd64:${env.PATH}"
  }
		echo "PATH is: ${env.PATH}"
	}
	stage ('CX Scan') {
		try {
			step([$class: 'CxScanBuilder', avoidDuplicateProjectScans: true, comment: '', credentialsId: 'ced6538b-2a32-4e80-9f82-28e8ee491bd5', excludeFolders: 'node_modules,test,target,build', exclusionsSetting: 'job', failBuildOnNewResults: false, failBuildOnNewSeverity: 'HIGH', filterPattern: '''!**/_cvs/**/*, !**/.svn/**/*,   !**/.hg/**/*,   !**/.git/**/*,  !**/.bzr/**/*, !**/bin/**/*,
!**/obj/**/*,  !**/backup/**/*, !**/.idea/**/*, !**/*.DS_Store, !**/*.ipr,     !**/*.iws,
!**/*.bak,     !**/*.tmp,       !**/*.aac,      !**/*.aif,      !**/*.iff,     !**/*.m3u, !**/*.mid, !**/*.mp3,
!**/*.mpa,     !**/*.ra,        !**/*.wav,      !**/*.wma,      !**/*.3g2,     !**/*.3gp, !**/*.asf, !**/*.asx,
!**/*.avi,     !**/*.flv,       !**/*.mov,      !**/*.mp4,      !**/*.mpg,     !**/*.rm,  !**/*.swf, !**/*.vob,
!**/*.wmv,     !**/*.bmp,       !**/*.gif,      !**/*.jpg,      !**/*.png,     !**/*.psd, !**/*.tif, !**/*.swf,
!**/*.jar,     !**/*.zip,       !**/*.rar,      !**/*.exe,      !**/*.dll,     !**/*.pdb, !**/*.7z,  !**/*.gz,
!**/*.tar.gz,  !**/*.tar,       !**/*.gz,       !**/*.ahtm,     !**/*.ahtml,   !**/*.fhtml, !**/*.hdm,
!**/*.hdml,    !**/*.hsql,      !**/*.ht,       !**/*.hta,      !**/*.htc,     !**/*.htd, !**/*.war, !**/*.ear,
!**/*.htmls,   !**/*.ihtml,     !**/*.mht,      !**/*.mhtm,     !**/*.mhtml,   !**/*.ssi, !**/*.stm,
!**/*.stml,    !**/*.ttml,      !**/*.txn,      !**/*.xhtm,     !**/*.xhtml,   !**/*.class, !**/*.iml, !Checkmarx/Reports/*.*''', fullScanCycle: 10, teamPath: 'CxServer\\CxServer2', hideDebugLogs: true, isProxy: false, jobStatusOnError: 'UNSTABLE', password: '{AQAAABAAAAAQ4gCUHuusrAo9Eyg1c2VB4CXmMjzUNCxAn+GbWSWKTmI=}', preset: '36', projectName: 'Webgoat_java_Pipeline', sastEnabled: true, serverUrl: 'https://cxmanager.cx.local', sourceEncoding: '1', useOwnServerCredentials: true, username: '', waitForResultsEnabled: false])
		}
		catch (Exception e) {
		
                        echo 'Checkmarx is currently unstable:'  
			//+ e.toString()
                        //catchError(stageResult: 'UNSTABLE', buildResult: currentBuild.currentResult) {
                       // error 'Checkmarx is unstable'
                       // }
                       currentBuild.result = 'UNSTABLE'
		}
	}
	    stage("After pipeline") {
            echo 'hello'
        }
}// node
