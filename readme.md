### Accounts
An account represents access control over a set of assets including on-chain currency and NFTs. In Aptos, these assets are represented by resources that emphasize both access control and scarcity.


### Modules

Modules are libraries that define struct types along with functions that operate on these types.
A minimal module example which only stores an admin of the module.


### Functions

1. Public functions - can be consumed / accessed by other contracts.

2. Public Entry functions -  used directly by frontend apps. The input/outputs should be primitive types and can be optional. These functions are always public

Think of entry functions in Move as “setter functions” in languages like Java.

3. Inline Functions- The inline keyword is used to suggest to the compiler that a function should be in-lined. In-lining is a compiler optimization technique where the code of a called function is inserted directly into the calling function.


4. The acquires Keyword - A Move function (m::f) must be annotated with acquires <T> if and only if: The body of m::f contains a move_from<T>, borrow_global_mut<T>, or borrow_global<T> instruction
OR The body of m::finvokes another function (m::g), that is declared in the same module that is annotated with acquires



### Struct

Struct supports primitive types (integer, bool, address, vector and signer) and other structs (structs provided by Aptos framework like table and user defined structs). All structs are private in the module. Other modules need to access those via public getter and setter functions.

Abilities
    Struct has abilities, which allows developers to give fine-grained control over the "linear" typing behavior of the value (i.e. instance of struct).
    There are 4 abilities.
1. Key - storing in global address space — resource
    2. Store - storing under another struct in global address space
    3. Drop - the data to be implicitly deleted / dropped, otherwise must explicitly deconstruct
    4. Copy - for data to be implicitly copied, useful for things like strings


### Signer
In transaction, sender is represented by a signer. The Aptos Move VM will translates the identity of the account that signed the transaction into a signer in a Move module entry point.
When a signer is not specified in a function, for example, the below deposit function, then no signer-based access controls will be provided for this function:



### Resources
Resources are struct instance with The key ability that are stored in global storage or directly in an account.

The store ability allows struct instances to be stored within resources.


### Object
Objects are the primary means of storing and managing resources in Move
Object is a container for resources that are stored within a single address.

It includes a resource ObjectCore which stores both the address of the current owner and the appropriate data for creating event streams.


### Resources
Structs with the key ability are known as “Resources”.


### Doubts
Why are 2 objects needed collections and token



## How to Work a Project
mkdir userinfo
cd userinfo
aptos move init --name UserInfo

aptos move compile



toe bomb symbol genuine finger pill blush provide menu video dignity license