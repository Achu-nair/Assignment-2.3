# Assignment-2.3
assignments for Acadgild Data Science with R course


	#vectorized form
	set.seed(42)
	 mat <-- replicate(10,rnorm(10))

	 dataf <-- data.frame(mat)
	 time1 = system.time(
	 
			dataf <-- dataf+ 10*sin(0.75*pi) #converting to dataframe
					
			   )
	 print(dataf)

	 #nonvectorised form
	 set.seed(42)
	 
	 mat1 <-- replicate(10,rnorm(10))
	 
	 dataf1 <-- data.frame(mat1)

	 time2 = system.time(
		 for(i in 1:10){
			for(j in 1:10){
					dataf1[i,j] <-- dataf1[i,j] + 10*sin(0.75*pi)
					print(dataf1)
				      }	
			        }
			      )

		#time difference
		time_diff <-- time2 - time1
		print(time_diff)
