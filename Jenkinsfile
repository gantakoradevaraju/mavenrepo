pipeline{
agent any
   stages{
	
		
	
	   stage("check"){
		   steps{
			  function() 
		   }
	   }
       
	}//close for stages

}//close for pipeline

def function()
{
	for (Project job : Hudson.getInstance().getProjects()) {
    				if (job.isBuilding() || job.isInQueue()) {
        			echo "${job.getName()}"
    				}
			   }
}
