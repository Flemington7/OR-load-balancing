## **Overview**
This Python script is part of a load balancing problem, which is _**a common issue in distributed computing where work is distributed
among multiple computers or servers**_ to achieve optimal resource utilization, minimize response time, and avoid overload.
Specifically, this script is part of a project that aims to find the optimal schedule for cloud load balancing to keep a service
running in the cloud at reasonable cost by _**reducing the expense of running cloud servers**_ while _**minimizing risk and human time 
due to migrating**_ and _**doing balance sleeping models across servers**_.

<center>
<img src="load_balancing.png"
     width="300" height="400" />
</center>

### The objective function:
- Minimize the total cost of running servers
- Minimize the total cost of migrating users from one server to another to reduce the risk and human time
- Minimizing the upper bound of the number of sleeping process on each server to balance the sleeping process across servers

_p.s.: These three objectives are combined into one objective function by order of importance in distributed computing._
### The constraints:
- The number of processes running on each server must less than max_process_per_server
- Each user is assigned to exactly one server and this server must be active
- The number of processes sleeping on each server must less than max_sleeping_workload
### The decision variables:
- assign_user_to_server[i,j] = 1 if user i is assigned to server j, 0 otherwise
- active_servers[j] = 1 if server j is active, 0 otherwise

## **Download and Installation**
Only use the community edition of the CPLEX python package.
- Python 3.10 or later
- `conda install docplex==2.25.236`
