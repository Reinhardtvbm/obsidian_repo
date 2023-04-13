# Locality
The principles of locality are exploited to create computer memory systems that are both fast and large. 
- **Temporal locality**: Recently accessed data is likely to be accessed again
- **Spatial locality**: Data that is near recently accessed data is more likely to be accessed than data far away

Since there is not enough money or space in the universe to create an infinitely sized memory with the same access time as the fastest cache, a memory hierarchy is implemented to provide a large memory with satisfactory speed. 

Data that is _most_ likely needed in the near future is kept in the smallest, but fastest level of memory, and data that is _least_ likely needed in the near future is kept in the largest, yet slowest level of memory.
![[Pasted image 20230413144428.png]]

# Cache
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

### Fully Associative
Fully associative cache has a set size equal to the size of the entire cache
![[Pasted image 20230413145957.png]]

### Set Associative
Set assiciative cache has a set size of $K$ blocks for a $K$-way set associative cache 
![[Pasted image 20230413150018.png]]

## Finding a Block in Cache
