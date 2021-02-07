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

//Activating the network ...
- From the driver, we create a network object. The If statement in the the network constructor then it switch thread to the server; also has the yield function in run() when we call start() in the driver

//Initializing the server ...
-From the driver, we create a server object. In the server constructor, create a network object with parameter "server", which will activate the else statement of the network constructor

//Activating network components for server...
-From the server contructor we call the network constructor("server"). It goes in the else statement in network constructor since it doesn't have the parameter "network"

//Inializing the Accounts database ...
sysout from the server constructor

initializeAccount() : Take the account text file and create account object

//Connecting server to network ..
sysout from the server constructor. Also print out after the above line

//Initializing client sending application ...
-From the driver we make a client object and we use the Client constructor, create client obejct with parameter "sending".  


//Activating network components for client...
From the Client constructor, we also create a network object with parameter "client", printing out the above statement. Goes in the else statement of the network constructor since it is not a "network" parameter.


//Initializing the transactions
after creating the network object, inside the client constructor then calls readTransaction(): Read the text file input for transaction

//Connecting client to network
a simple sysout after readTransactions().


//Initializing client receiving application ..
create another Client object with parameter receiving from the Driver.
Go to the elses statement of the client constructor and print out:

If the client is sending, go to sendTransaction().
In that function, it checks if the buffer is full or not, the set status as sent, then send transaction and increment the index
The other client object is for receiving, which will go to receiveTransaction(), then it will check if the buffer is empty or not, if it is empty it will switch back to the send client thread if it is not it will receive the transaction and print out the transaction statement then increment the i.
After done all the transaction it will disconnect and terminate the sending client thread first.
Then the server after processing all the transaction, it will disconnect print out terminate the server thread,
Then the receiving client thread will disconnect then terminate,
Then because both clients are disconnected and the server is also disconnected  it will terminate the network thread.
```
