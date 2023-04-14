## Types of Caches
The different types of caches can be categorised by the method used to place a block of memory not already in the cache. Or also the set size. Since a block will always be mapped to the set numbered:
$$S_i = B_{addr} \text{ MOD } N_{blocks}$$
Where 
- $S_i$: The set
- $B_{addr}$: Block address
- $N_{blocks}$: Number of blocks

Memory is arranged into block to take advantage of _spatial locality_. The larger the block size, the higher the hit rate of each memory level will be.

### Directly Mapped
Directly mapped cache has a set size equal to one block. 
![[Pasted image 20230413145919.png]]

In a directly mapped cache, each block in main memory has exactly one location that it can be placed in cache
### Fully Associative
Fully associative cache has a set size equal to the size of the entire cache
![[Pasted image 20230413145957.png]]

In a fully associative cache, any block in main memory can be placed anywhere in the cache. For this reason, there are no _set_ bits in an address, and the entire cache must be searched in parallel for a hit

### Set Associative
Set assiciative cache has a set size of $K$ blocks for a $K$-way set associative cache 
![[Pasted image 20230413150018.png]]

A K-way set associative cache has K number of locations possible for each block in main memory
## Finding a Block in Cache
An address can be split into the _block address_, and the _block offset_
![[Pasted image 20230414005508.png]]

A fully associative cache has 0 set bits, since there is only one set, a set associative cache will have $log_2(\text{number of sets})$ set bits, and a direct mapped cache will have  $log_2(\text{cache size in blocks})$ set bits, which are called line bits in since there are no "sets" in a direct mapped cache.