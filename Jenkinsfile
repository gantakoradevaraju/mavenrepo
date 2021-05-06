
def jobcount = 0
pipeline{
agent any
   stages{
	
		
	
	   stage("check"){
		   steps{
			   function()
			   script {
				   echo "${jobcount}"
			   }
			  
		   }
	   }
       
	}//close for stages
	post{

                when{
			expression { jobcount == 0 }
		}
                 script{
			echo "stop"
                 }
                
                
    }


}//close for pipeline

def function()
{
	println Hudson.instance.queue.items.length
	jobcount = Hudson.instance.queue.items.length
	println jobcount
	for (Project job : Hudson.getInstance().getProjects()) {
			echo "${job.getName()}"
    				if (job.isBuilding() || job.isInQueue()) {
        			echo "${job.getName()}"
    				}
			   }
}
