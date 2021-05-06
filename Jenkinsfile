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
	println Hudson.instance.queue.items.length
	for (Project job : Hudson.getInstance().getProjects("mlb")) {
			echo "${job.getName()}"
    				if (job.isBuilding() || job.isInQueue()) {
        			echo "${job.getName()}"
    				}
			   }
}
