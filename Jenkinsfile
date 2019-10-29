node("master"){

  properties([parameters([string(defaultValue: 'BVT_JOB_NAME', name: 'DEPLOY_ENV')])])
  stageName = "Trigger BVT"
  stage(stageName){
	  echo "Checking something of val: ${BVT_JOB_NAME}"	
  }
}
