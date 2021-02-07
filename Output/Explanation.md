```
There are some of the reasons why we believe that there are different running times: 

-External programs or processes running outside this software (IDE) may have an impact on the individual thread running time each time we run our program. 

-There is no way to say which order the threads are being executed in, so in some of our executions there might be threads waiting for others. 
Whereas in subsequent running of this program, the command for thread execution can be modified to provide more effective running times.

-Hardware performance can also impact thread running time, if the program is running with different CPUs, the time for termination can vary from one another. 
Small timing discrepancies may be ok for our purposes, but a variety of other applications (such as trading) may need those millisecond gaps.
```
```
Brief Explanation

 Activating the network ...
- If statement in the the network constructor then it switch thread to the server

 Initializing the server ...
-In the server constructor, create a network object with parameter "server", which will activate the else statement of the network constructor

 Activating network components for server...
- the else statement in network constructor

Inializing the Accounts database ...
initializeAccount() : Take the account text file and create account object


 Connecting server to network ..
also print out after the above line

-Initializing client sending application ...
from the driver use the Client constructor, create client obejct with parameter "sending".  

also create a network object with parameter 'client', printing out:
Activating network components for client...

after creating the network object:
Initializing the transactions
readTransaction(): Read the text file input for transaction

Connecting client to network

create another Client object with parameter receiving:
Go to the elses statement of the client constructor and print out:
 Initializing client receiving application ..

if the client is sending, go to sendTransaction()
in that function, it checks if the buffer is full or not, the set status as sent, then send transaction and increment the index


The other client object is for receiving, which will go to receiveTransaction() 
, then it will check if the buffer is empty or not, if it is empty it will switch back to the send client thread
if it is not it will receive the transaction and print out the transaction statement then increment the i

After done all the transaction it will disconnect and terminate the sending client thread first

Then the server after processing all the transaction, it will disconnect print out terminate the server thread

Then the receiving client thread will disconnect then terminate
 
Then because both clients are disconnected and the server is also disconnected  it will terminate the network thread
```
