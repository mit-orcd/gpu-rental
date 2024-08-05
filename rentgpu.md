### Initial notes on GPU rental

1. You will need an account on the MIT Engaging Cluster. This is available to anyone with MIT credentials. To activate your account go to the [Engaging Portal](https://engaging-ood.mit.edu/)
   
   <img width="500" alt="image" src="https://github.com/user-attachments/assets/539ebab0-77ca-4204-9920-3fd1e345b3f8">

   and sign in, and then wait 15 minutes for system to update. 

2. Once you have activated your account, you can log in to an Engaging command shell using simple ssh access e.g.
   
      ```ssh -l XXXXX eofe10.mit.edu```

   where ```XXXX``` is your MIT account name. You can also access a command shell from the [Engaging Portal](https://engaging-ood.mit.edu/)

3. From an Engaging command shell session, use the Slurm reservation manager to access your reserved node(s) e.g.

   ```salloc --reservation=RRRRR -p sched_mit_orcd --gres=gpu:4```
   
   where RRRRR the reservation name provided to you in the reservation confirmation.

4. Individual accounts need to be registered to use each reservation. For now, email cnh@mit.edu to have an account added to a reservation. 

5. Once connected to the reserved node(s) the allocated GPUs should be visible using the ```nividia-smi``` command.
   
6. A set of pre-installed software is visible through the ```module avail``` command as described in the regular [ORCD help pages](https://orcd-docs.mit.edu).


