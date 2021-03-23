node {
	stage ('Git SCM') {

		git 'https://github.com/Kapombo/WebGoat-Legacy.git'

	}
	stage ('CX Scan') {
		step([$class: 'CxScanBuilder', avoidDuplicateProjectScans: true, comment: '', credentialsId: '6671b964-005a-489c-b4c5-18919e404ce1', excludeFolders: 'node_modules,test,target,build', exclusionsSetting: 'job', failBuildOnNewResults: false, failBuildOnNewSeverity: 'HIGH', filterPattern: '''!**/_cvs/**/*, !**/.svn/**/*,   !**/.hg/**/*,   !**/.git/**/*,  !**/.bzr/**/*, !**/bin/**/*,
!**/obj/**/*,  !**/backup/**/*, !**/.idea/**/*, !**/*.DS_Store, !**/*.ipr,     !**/*.iws,
!**/*.bak,     !**/*.tmp,       !**/*.aac,      !**/*.aif,      !**/*.iff,     !**/*.m3u, !**/*.mid, !**/*.mp3,
!**/*.mpa,     !**/*.ra,        !**/*.wav,      !**/*.wma,      !**/*.3g2,     !**/*.3gp, !**/*.asf, !**/*.asx,
!**/*.avi,     !**/*.flv,       !**/*.mov,      !**/*.mp4,      !**/*.mpg,     !**/*.rm,  !**/*.swf, !**/*.vob,
!**/*.wmv,     !**/*.bmp,       !**/*.gif,      !**/*.jpg,      !**/*.png,     !**/*.psd, !**/*.tif, !**/*.swf,
!**/*.jar,     !**/*.zip,       !**/*.rar,      !**/*.exe,      !**/*.dll,     !**/*.pdb, !**/*.7z,  !**/*.gz,
!**/*.tar.gz,  !**/*.tar,       !**/*.gz,       !**/*.ahtm,     !**/*.ahtml,   !**/*.fhtml, !**/*.hdm,
!**/*.hdml,    !**/*.hsql,      !**/*.ht,       !**/*.hta,      !**/*.htc,     !**/*.htd, !**/*.war, !**/*.ear,
!**/*.htmls,   !**/*.ihtml,     !**/*.mht,      !**/*.mhtm,     !**/*.mhtml,   !**/*.ssi, !**/*.stm,
!**/*.stml,    !**/*.ttml,      !**/*.txn,      !**/*.xhtm,     !**/*.xhtml,   !**/*.class, !**/*.iml, !Checkmarx/Reports/*.*''', fullScanCycle: 10, groupId: '1', highThreshold: 0, isProxy: false, jobStatusOnError: 'FAILURE', lowThreshold: 0, mediumThreshold: 0, password: '{AQAAABAAAAAQ4gCUHuusrAo9Eyg1c2VB4CXmMjzUNCxAn+GbWSWKTmI=}', preset: '36', projectName: 'Webgoat_java_Pipeline', sastEnabled: true, serverUrl: 'https://cxmanager.cx.local', sourceEncoding: '1', useOwnServerCredentials: true, username: '', vulnerabilityThresholdEnabled: false, vulnerabilityThresholdResult: 'FAILURE', waitForResultsEnabled: true])

	}
	    stage("After pipeline") {
            echo 'hello'
        }
}// node


