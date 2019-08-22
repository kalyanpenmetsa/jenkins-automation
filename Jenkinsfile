#!/usr/bin/env groovy

properties([[$class: 'ParametersDefinitionProperty', parameterDefinitions: [

// Env Config
[$class: 'hudson.model.StringParameterDefinition', name: 'PHASE', defaultValue: "", description: "Please enter the phase: BUILD, BUILD_DEPLOY, DEPLOY"],
[$class: 'hudson.model.StringParameterDefinition', name: 'ENV', defaultValue: "", description: "Please enter the environment details"]
]]])

node("master") {
	// withEnv(["PATH=${env.PATH}:${tool 'mvn'}", "MVN_HOME=${tool 'mvn'}"]) {
		stage('Checkout') {
			checkout scm
		}
			if ("${PHASE}" == "BUILD" || "${PHASE}" == "BUILD_DEPLOY") {
				stage('Compile') {
		      echo "${env.BRANCH}"
		    }
				stage('Unittest') {
					echo "Unittest will happen here..."
				}
				stage('CodeCoverage') {
					echo "Code Coverage will happen here..."
				}
				stage('SonarAnalysis') {
					echo "Sonar Analysis will happen here..."
				}
				stage('Package') {
					echo "Code Packaging will happen here..."
				}
				stage('SmokeTest') {
					echo "Smoke testing will happen here..."
				}
			}
			if ("${PHASE}" == "BUILD_DEPLOY" || "${PHASE}" == "DEPLOY") {
				stage('CopyToDev') {
		      echo "Pre-Check will take place here..."
		    }
				stage('SmokeTestOnDev') {
					echo "Source cleanup destination migration..."
				}
			}
  // }

}
