node("master"){

  properties([parameters([string(defaultValue: '', name: 'BVT_JOB_NAME')])])
  stageName = "Trigger BVT"
  stage(stageName){
	  echo "Checking something of val: ${BVT_JOB_NAME}"	
  }
}
