# kappavi
a key value store in ram

## The Idea

### Step 1
The idea is to write in GOlang a minimal skeleton app that use http interface to store,list,retrieve and delete data from a key-value 
store in RAM
* custom protocol

### Step 2
Here we want to add the ability to talk to other instances of the application on any network, via a centralized server and UDP.

* Structure a plugin system
* Write the CENTRALIZED SERVER (if possible keep it so generic it could be used by other projects)
* The centralized server only has the list of the machines, it has no data about the content in each instance of the 'kappavi' program.
* The comunication after that is peer-to-peer using UDP to be able to pass through NAT firewall.
* This is used for data replica and sharding
* A groups of machines that share replica/sharding is defined 'clan'
* Each clan can choose is ClanID (a string), for read and write and the \<put a hash function here, ex. SHA-1\> of this ClanID is the readonly version of the ClanID
 * The ClanID can be in a config file, passed on command line, or compiled into the executable.
 * Readonly nodes recieve key and values from other nodes, but can't add data to the dictionary or delete them.

### Step 3

* Implement other protocols as plugin
 * memcached
 * redis
