
def jobcount = ""
pipeline{
agent any
   stages{
			
	
	   stage("check"){
		   steps{
			  
			   script {
				   echo "${jobcount}"
				    function()
			   }
			  
		   }
	   }
       
	}//close for stages
	
}//close for pipeline

def function()
{
	println Hudson.instance.queue.items.length
	jobcount = Hudson.instance.queue.items.length
	
	
}
