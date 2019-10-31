node("master"){
//  properties([parameters([string(defaultValue: '', name: 'BVT_JOB_NAME')])])
  def BVT = 'true'
  if(BVT == 'true' && BVT_JOB_NAME == ""){
    error "BVT Job is not defined to run the BVT tests. Please enter the right parameter value and trigger again!"
  }
	
  context = helper.prepareStage(["stageName": "Prepare",
				 "BVT_JOB_NAME": "AUTOM_ServerEPS_BVT"])

  stage(stageName){
	  echo "Checking something of val: ${BVT_JOB_NAME}"	
  }
}
