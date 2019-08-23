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
		echo "FUCK"
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

}
