#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PHASE', defaultValue: "", description: "Please enter the phase: BUILD, BUILD_DEPLOY, DEPLOY"],
[$class: 'hudson.model.StringParameterDefinition', name: 'ENV', defaultValue: "", description: "Please enter the environment details"]
]]])

node("master") {
<<<<<<< HEAD
try {
	stage('Checkout') {
		checkout scm
	}
		if ("${env.BRANCH_NAME}" == "master") {}
		if ("${env.BRANCH_NAME}" == "dev") {}
		if ("${env.BRANCH_NAME}" == "qa") {
			stage('Smoke Test') {
				echo "Python script for QA"
				bat "pytest VivedApp.py -s -k test004"
			}
		}
		if ("${env.BRANCH_NAME}" == "product") {
			stage('Smoke Test') {
				echo "Python script for Product"
				bat "pytest VivedApp.py -s -k test004"
			}
		}
	emailext  to: 'penmetsa29@gmail.com',
						replyTo: 'vpen29@gmail.com',
				    recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']],
						mimetype: 'text/html',
						subject: "Hello Sender",
						body: "Hello"
}	catch(error) {
	// emailext  to: 'jr7365@att.com,av206a@att.com',
	// 					replyTo: 'DL-IDPENVMGMT@att.com',
	// 			    recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']],
	// 					mimetype: 'text/html',
	// 					subject: 'IDP Job - '  + env.JOB_NAME + ' - Build No: ' +  env.BUILD_NUMBER + ' - ' + status,
	// 					body: 'Job : ' + env.JOB_NAME  + '\n' +
	// 								'Build No : ' + env.BUILD_NUMBER  + '\n' +
	// 								'Phase : ' + "${PHASE}"  + '\n' +
	// 								'Status : ' + status  + '\n\n' +
	// 								'Jenkins Job : ' + env.BUILD_URL + '\n' +
	// 								'Changes : ' + env.BUILD_URL + 'changes' + '\n' +
	// 								'Console Log : ' + env.BUILD_URL + 'consoleFull' + '\n\n' +
	// 								'K8 (' + env.TARGET_ROLE +  ') Node Port URL for Validation: ' + env.K8_APP_URL + '\n\n' +
	// 								content
	throw error
}
=======
	// withEnv(["PATH=${env.PATH}:${tool 'mvn'}", "MVN_HOME=${tool 'mvn'}"]) {
		stage('Checkout') {
			checkout scm
		}
			if ("${env.BRANCH_NAME}" == "master") {}
			if ("${env.BRANCH_NAME}" == "dev") {}
			if ("${env.BRANCH_NAME}" == "qa") {
				stage('Smoke Test') {
		      echo "Python script for QA"
		    }
			}
			if ("${env.BRANCH_NAME}" == "product") {
				stage('Smoke Test') {
		      echo "Python script for Product"
		    }
			}
  // }
>>>>>>> 8a093e5c5e26795bc998464b6d3eb8cefa505384
}
