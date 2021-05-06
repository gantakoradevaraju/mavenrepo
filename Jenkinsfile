
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
			 jobcount == 0 
		}
                 script{
			echo "stop"
                 }
                
                
    }


}//close for pipeline

def function =
{
	println Hudson.instance.queue.items.length
	jobcount = Hudson.instance.queue.items.length
	
	
}
