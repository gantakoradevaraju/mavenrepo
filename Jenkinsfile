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
			echo "${job.getName()}"
    				if (job.isBuilding() || job.isInQueue()) {
        			echo "${job.getName()}"
    				}
			   }
}
