# Searching for and executing a plan

If a CA has an intent without a plan, search for a feasible plan and execute it
	
Searching for a feasible plan to achieve a goal

	Construct a plan that might achieve the goal
	Submit it as todo to umwelt for consideration
	Wait for confirmation that all its directives can be sought (feasible)
	or for a directive that can't be sought by the entire umwelt (not feasible)
	If feasible, execute it
		if execution_failed for any of the plan's directives,
		    search for another plan
	If not feasible,
		search for another plan
	If replacing an intent that is not yet executed,
		tell the umwelt to abandon the directives associated with the plan
		
Executing a plan to achieve a goal

   If CA level > 1
	   Select the next ready directive in the plan
	   	Select an umwelt CA who can_seek the directive
	   	Send it execute(directive, plan_id)
		   If execute_failed is received for the directive
		   	select another umwelt CA that can_seek it and tell it to execute it
		   	if none left and the plan's goal was a directive
		   		send failed_to_execute(goal_id) to the parent who sent the goal
	   If all directives in the plan were executed,
	        if the plan's goal was a directive
	    		send executed(goal_id) to parent who sent the goal
	   	
   If level 1 - a plan is a single act composed of actions to be taken all at once
	   Send static umwelt ready_actuations([action, ...])
	   Call body:execute
	   Send parent executed(goal_id)

parent CA <=> umwelt CA:

P =E=> U todo(directives) - to all umwelt CAs
	U: For each directive, 
		if not relevant to the umwelt CA, respond with cannot_seek for the directive
		if relevant, respond with can_seek for the directive
		
P =E=> U abandon(plan_id)
	U: Forget all directives associated with the parent's plan

P <=M= U can_seek(goal_id)/cannot_seek(goal_id), ... 
	P: The CA changes the goal state 
	   and, implicitly, the container plan's status, perhaps to feasible or not_feasible

P =M=> U execute(directive, plan_id), ... to one umwelt CA - umwelt CAs compete for engagement
	U: Search for a feasible plan for the directive
	   If plan not found, 
	   	send back `failed_to_execute(directive)`
	   Else retain the directive (associating it with a parent's plan) and execute the plan for it
		   	   
P <=M= U executed(goal_id) - the goal was executed
	P: If execution of goal_id completes execution of a plan P built to achieve a received a directive,
		send executed(directive_id) to the parent 

P <=M= U failed_to_execute(goal_id) - the goal could not be executed
	P: If failure to execute of goal_id fails execution of a plan P built to achieve a received a directive,
		send failed_to_execute(directive_id) to the parent 
