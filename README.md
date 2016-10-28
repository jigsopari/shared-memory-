Steps:

1. run gcc -Wall -o s newserver.c
2. gcc -Wall -o c newclient.c
3. run first ./s and then run ./c
4. the flow in shared memory is like the data is put into shm by running server and then the client accesses the data and attches the * sign at the 
   end of the memory seeing which server sleeps for 1 sec and will exit. but this does not mean that the shared memory is cleared.
5. we can see shm by $ipcs -m { on the server side}
6. ipcrm -M key(9876) to remove the shm with the given key
7. to see other ipc's on the system do $ ipcs n-attach.. shows semaphores,queues and shared memory if any is present.
